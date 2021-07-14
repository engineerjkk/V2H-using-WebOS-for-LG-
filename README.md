# V2H-using-WebOS-for-LG-
## 1. 제어 파트

### 차량이 주차장에 도착하면 사용자는 미리 "에어컨 켜줘", "불 켜줘" 라고 말한다.
-> ThinkQ AI 기반 음성인식
-> 차량에 설치된 라즈베리 파이사용
-> ESP32 서버에 데이터 전송

### 서버로 부터 받은 명령을 ESP32에서 릴레이를 제어한다.
-> 릴레이는 에어컨, 전구, 공기청정기, 전기장판, TV, 안마의자와 연결돼있다. 

## 2. 데이터베이스 구축 파트
### 1) 차량내에 ESP32를 설치해 실시간 전류 사용량을 측정해 데이터베이스에 누적한다.
### 2) 집안에 ESP32를 설치해 실시간 가전 전류 사용량을 측정해 데이터 베이스에 누적한다.

**이렇게 함으로써 예를 들어, 쏘카와 에어비엔비가 제휴를 맺을때 차량 전류사용량(전기차기준)과 가전의 전류사용량을
한꺼번에 고객에게 한꺼번에 청구해 줄 수 있다.**

## 의미 도출 : 
1. 집에 도착하기전 미리 에어컨을 켜줌으로써 시원한 실내환경을 만들고 불을 킴으로써 들어가자마자 환한 실내환경에 들어갈 수 있다.
2. 공유경제 서비스가 활성화 되고 있어 고객에게 편리하고 투명한 요금청구 서비스를 할 수 있다.
3. 1번의 경우 모바일에서도 할 수는 있지만 모바일보다 모빌리티 서비스 시장이 커지는 만큼 모바일을 거치지 않고 바로 모빌리티에서 작업을 수행한다.
4. 집에 있는 데쉬보드에서는 미리 차를 히팅시켜두거나 에어컨놓기, 차량위치? (라이다릉통해 미리 위치를 셋팅했다면 데쉬보드 상에서 한번에 알려줄수도 있을것)   
-> 즉 집과 차량 모두 라즈베리파이 WebOS는 있다.

# HardWare
### BOM
![image](https://user-images.githubusercontent.com/76835313/124378459-5c11e000-dcec-11eb-9657-5b64cefc6ab8.png)
### Circuit Design
![image](https://user-images.githubusercontent.com/76835313/124378469-67650b80-dcec-11eb-9178-f6a75f4ad2a7.png)
### PCB Layout Example
![image](https://user-images.githubusercontent.com/76835313/124378507-9b403100-dcec-11eb-87a6-1cf5fb4c2169.png)
### 참고 링크
https://www.youtube.com/watch?v=HK3qpyeSOcY


# Rasberry Pi
라즈베리 파이 상에서 음성인식 서비스 구현 전에 프로토 타입으로 버튼을 누르면 해당 서버로 접속한다.
각 접속한 서버를 통해 원하는 제어를 할 수 있다. 현재는 LED ON/OFF만 가능하다.
![image](https://user-images.githubusercontent.com/76835313/124382429-57f0bd00-dd02-11eb-91f2-8b53da33a773.png)

![image](https://user-images.githubusercontent.com/76835313/124382416-47d8dd80-dd02-11eb-9fd1-4cc050e3fad2.png)

* [WebOS란 무엇인가](https://webos-supporters.tistory.com/8)
* [Index of WebOSose](http://build.webos-ports.org/webosose/)
