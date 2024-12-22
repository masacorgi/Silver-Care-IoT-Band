# Silver-Care-IoT-Band

실버케어 IoT 밴드 프로젝트에 대한 문서와 코드의 아카이브입니다.   
   
해당 프로젝트는 2022년 한국공학대학교 졸업 과제로 제작되었습니다.   
   
<!--
해당 README는 간략한 프로젝트 구성을 나타내고 있으므로, 더 자세한 수행과정에 대한 정보는 다음 링크를 통해 접근하실 수 있습니다.  -> [수행보고서](/수행보고서파일경로)   
-->   
   
### 목차
&emsp;&emsp;[1. 주제 및 기획의도](#1.-주제-및-기획의도)   
&emsp;&emsp;[2. 기능 개요](#2.-기능-개요)   
&emsp;&emsp;[3. 역할 분담](#3.-역할-분담)   
&emsp;&emsp;[4. 적용기술/개발환경](#4.-적용기술/개발환경)   
&emsp;&emsp;[5. 모니터링 화면](#5.-모니터링-화면)   
&emsp;&emsp;[6. 밴드 하드웨어](#6.-밴드-하드웨어)   
   
   
## 1. 주제 및 기획의도
```
- 주제 : 홀몸노인을 위한 건강 모니터링 IoT 밴드

- 기획의도 :
  노인 인구의 증가와 함께 증가한 1인가구 노인의 건강상태와 위험상황을 실시간으로 원격 확인할
  수 있는 IoT 밴드를 제작해 보호자와 담당 공무원의 신속한 대처를 돕기 위함

- 차별점 :
  해당 프로젝트의 IoT 밴드는 저렴한 PCB, MCU를 활용하고 작동 방식이 직관적인 밴드를 제공하기에
  시중 판매되는 스마트 워치에 비교하여 저렴한 구매비용, 단순한 사용법을 보유한다.
```

## 2. 기능 개요
```
- IoT 밴드 :
  * 상시 심박수 체크
  * 상시 산소포화도 체크
  * 상시 낙상감지
  * 위급상황 발생시 호출 버튼 사용가능

- 모니터링 웹앱 :
  * 실시간 심박수 체크
  * 실시간 산소포화도 체크
  * 낙상감지 시 알림 수신
  * 위급 버튼 눌릴 시 알림 수신
```

## 3. 역할분담
```
  이진성 : Arduino 동작코드, MQTT Data Network Setting
  김상운 : RaspberryPi 탑재 Node-red 서버 개발
  장대영 : 밴드 하드웨어 설계, 제작
```


## 4. 적용기술/개발환경
```
HardWare
- IoT Band :
   * node mcu : ESP8266
   * 3축 자이로 센서 : modelnumber 1234
   * 심박 센서 : modelnumber 1234
   * 산소포화도 센서 : modelnumber 1234
- Server :
   * Raspberry Pi 3B+

SoftWare
- IoT Band :
   * C(Arduino), MQTT protocol
- 모니터링 웹앱 :
   * Node-red Server
```

## 5. 시스템 구성
![image](https://github.com/user-attachments/assets/c9069c11-8ec3-4f4a-9e55-89a3a3ddc9da)
```
이 기기의 동작방식은 BOOT 스위치를 눌러 와이파이를 통해 서버와 연결한다.
그 이후 내부 센서인 심박 센서, 자이로 센서 초기화가 일어나며 초기화된 센서들에서 측정이 시작된다.
위 시스템 구성도를 보면 측정 불가가 되었을 경우 미측정 데이터는 삭제가 되며 측정되지 않는다는 화면을 webapp에서 확인할 수 있다.
위급 상황 발생 시 스마트폰 또는 PC 브라우저에서 알림을 수신받을 수 있다.
```

## 5. 모니터링 화면
![image](https://github.com/user-attachments/assets/bb74c167-b7a4-417e-9347-f9ef89f70ccd)
![image](https://github.com/user-attachments/assets/588aa196-7bdc-4700-8a04-574597326435)

![image](https://github.com/user-attachments/assets/398c9389-3a8a-4cc8-b48a-3dd5edca383c)


## 6. 밴드 하드웨어

![image](https://github.com/user-attachments/assets/5263309c-7937-4c89-9a11-1ce54369e2e7)
![image](https://github.com/user-attachments/assets/a7a8837d-07fc-4b83-b136-954e542c57ab)
![image](https://github.com/user-attachments/assets/ebaabd7c-dd37-429b-8b3d-a23b17cfe073)


![착용샷](https://github.com/user-attachments/assets/55601ac2-346d-4034-a169-d8e238a8f885)


