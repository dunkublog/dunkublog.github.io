---
layout: single
title:  "싱글턴 패턴 with 유니티"
categories: unity
tag: [unity, c#]
toc: true
---

## 싱글턴 목표
유일성을 보장하는 것
- 초기화된 후, 런타임 동안 메모리에 단 하나의 인스턴스만 존재하는 것을 의미한다.
- 자신과 같은 유형의 인스턴스 개체가 있으면 즉시 제거한다.  
<br>
<br>



## 싱글턴 패턴 장단점
### 장점
- 전역 접근이 가능하다.
- 공유 자원에 동시 접근을 제어할 수 있다.
<br>

### 단점
- 싱글턴을 과도하게 사용할 경우 유닛 단위의 테스트가 어려워진다.
- 사용하기 쉽다는 점 때문에 싱글턴을 남발하는 잘못된 습관이 생길 수 있다.
<br>
<br>



## 게임 매니저에 사용하기
싱글톤 패턴은 주로 게임 매니저에 사용된다.
게임이 종료될 때까지 살아있어야 하며, 서버와의 통신, 전역 설정 초기화, 로깅, 플레이어 진행 상황을 저장하는 등의 기능을 맡을 수 있다.
<br>

### 예제
#### 싱글턴 클래스 제작
상속받으면 해당 객체를 싱글턴으로 만들어 주는 클래스를 작성한다.
```csharp
using UnityEngine;

public class Singleton <T> : MonoBehaviour where T : Component
{
    private static T instance;

    public static T Instance
    {
        get 
        { 
            if (instance == null)
            {
                instance = FindObjectOfType<T>();

                if (instance == null )
                {
                    GameObject obj = new();
                    obj.name = typeof(T).Name;
                    instance = obj.AddComponent<T>();
                }
            }

            return instance; 
        }        
    }

    public virtual void Awake()
    {
        if (instance == null)
        {
            instance = this as T;
            DontDestroyOnLoad(gameObject);
        }
        else
        {
            Destroy(gameObject);
        }
    }
}
```
<br>

#### 게임 매니저 클래스 제작
실제 게임 매니저로 사용할 클래스를 작성한다.
```csharp
using System;
using UnityEngine;
using UnityEngine.SceneManagement;

public class GameManager : Singleton<GameManager>
{
    private DateTime sessionStartTime;
    private DateTime sessionEndTime;

    void Start()
    {
        sessionStartTime = DateTime.Now;
        Debug.Log("게임 세션 시작: " + DateTime.Now);
    }

    void OnApplicationQuit()
    {
        sessionEndTime = DateTime.Now;
        TimeSpan timeDifference = sessionEndTime.Subtract(sessionStartTime);

        Debug.Log("게임 세션 끝: " + DateTime.Now);
        Debug.Log("게임 세션 지속 시간: " + timeDifference);
    }

    void OnGUI()
    {
        if (GUILayout.Button("다음 세션"))
        {
            SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex + 1);
        }
    }
}
```
<br>

#### 테스트
![싱글톤 씬 추가](https://drive.google.com/uc?export=view&id=123IR3tzpjdjvFRCCNZE3ycmibBdwah68)
테스트를 위해 Build Settings에 씬을 추가한다.

![싱글톤 다음 세션 버튼](https://drive.google.com/uc?export=view&id=1P4_g_lWusiYzySHJZqa-lWn4p0rEZZhE)
에디터를 실행하고, '다음 세션' GUI 버튼을 클릭한다.

![싱글톤 확인](https://drive.google.com/uc?export=view&id=13D1WjdYofoVDkM4liV4q5CscZjF8tmsu)
다음 씬으로 전환하는 동안 GameManager가 오직 하나만 존재하는 것을 확인할 수 있다.
