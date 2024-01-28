```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerHook : MonoBehaviour
{
    public LineRenderer line; // 후크와 플레이어와의 연결 라인
    public Transform hook; // 후크의 위치 정보
    Vector2 mousedir; // 마우스와 플레이어와의 거리

    [HideInInspector]
    public bool isHookActive; // 후크의 사용 여부
    [HideInInspector]
    public bool isLineMax; // 후크와 플레이어의 거리가 최대 일때의 여부
    [HideInInspector]
    public bool isCrash; // 충돌 여부
    [HideInInspector]
    public bool isCheck = false; // 후크 아이템 획득 여부


    public AudioClip HookSound; // Hook 소리 정보
    private AudioSource PlayHookSound; // Hook 소리 실행

    private void Start()
    {
        PlayHookSound = GetComponent<AudioSource>();
        line.positionCount = 2; // 라인의 포지션 갯수 = 첫 부분, 끝 부분
        line.endWidth = line.startWidth = 0.05f; // 라인의 굻기
        line.SetPosition(0, transform.position); // 첫 라인 위치 = 플레이어의 위치
        line.SetPosition(1, hook.position); // 끝 라인 위치 = Hook의 위치
        line.useWorldSpace = true;
        isCrash = true;
    }

    private void Update()
    {
        line.SetPosition(0, transform.position); // 첫 라인 위치 = 플레이어의 위치
        line.SetPosition(1, hook.position); // 끝 라인 위치 = Hook의 위치

        if (isCheck)
        {
            if (Input.GetMouseButtonDown(0) && !isHookActive)
            {
                hook.position = transform.position;
                mousedir = Camera.main.ScreenToWorldPoint(Input.mousePosition) - transform.position; // 마우스와 플레이어와의 좌표의 거리를 뺌
                isHookActive = true;
                hook.gameObject.SetActive(true);
                isCheck = false;
            }
        }

        if (isHookActive && !isLineMax && !isCrash)
        {
            PlayHookSound.clip = HookSound;
            PlayHookSound.Play();
            hook.Translate(mousedir.normalized * Time.deltaTime * 15); // 후크의 위치를 마우스커서 위치로 이동
            
            if (Vector2.Distance(transform.position, hook.position) > 3) // 후크와 플레이아와의 거리가 3보다 크다면
            {
                isLineMax = true;
            }
        } 
        else if(isHookActive && isLineMax && !isCrash)
        {
            hook.position = Vector2.MoveTowards(hook.position, transform.position, Time.deltaTime * 15); // 후크의 위치를 플레이어 위치로 이동
            if (Vector2.Distance(transform.position, hook.position) < 0.1f)
            {
                isHookActive = false;
                isLineMax = false;
                hook.gameObject.SetActive(false);
            }
        }
        else if (isCrash)
        {
            if (Input.GetMouseButtonDown(0))
            {
                isHookActive = false;
                isLineMax = false;
                isCrash = false;
                hook.GetComponent<CrashHook>().joint2D.enabled = false;
                hook.gameObject.SetActive(false);
            }
        }
    }
}

```
