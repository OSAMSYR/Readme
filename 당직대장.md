# ●당직대장

사용자의 숙면상태 판단 및 숙면 환경 판단.

관리자의 사용자 정보 관리 시스템 구축

사용자의 숙면 상태 판단 및 숙면 데이터 관리



## ○장점

​	※편리성: 위치에 상관없이 관리하는 방을 확인할 수 있다.

​	※직관적 UI: 직관적인 UI를 사용하여 편리함을 더했다.

​	※확장성: 모듈만 있다면 얼마든지 추가하여 사용할 수 있다.

​	※잠재성: 수면 데이터를 수집하여 가공할 수 있다.

## ○Block Diagram

​	

​	 ![img](https://lh3.googleusercontent.com/ITuTYVnJiPC8dPYoVnN7ASDAxsjqRPqE-_LsQcf4KnKop5dD8shm3NUcA5nH4XtivwzfMg6DA3lLGcbST7Z9CbYQvulCKjfRQIfCC8gapGP8cM63Vq8k11YFZdpxlwlepTOrbCTp) 



## ○ 개발 과정

​	1일차 : 아이디어 구체화, 콘셉트 및 통신 프로토콜 정의, 회로 구성

 ![img](https://lh3.googleusercontent.com/Ac7nyC3GNEifdcSSzMS-sGgbYuhtAN5wMvP3KBlL_buBpsixkmTzAdSNcLOTq3-3h5lTlFKDl9eXsel4IW4p-FVm86KxBVl9nI7btR5FtxAymWpocID5EUHkj-jMP79HJ-zj1_-G) 

​	2일차 :

​		Arduino :  침대에 누워있는 사람이 잘 자고있는지를 판단할 수 있다고 생각되는 센서들을 시리얼 통신을 통해 		기본적인 입출력을 확인하고 센서별 함수 및 블루투스 세팅. 버튼 함수 구현도중 자꾸만 루프문이 멈추는 현상		을 발견 후 바운스 현상 해결. 숙면을 취하고 있는지 판단하는 로직을 아두이노에서 모션센서를 통해 구현. 센		서들을 통해 얻은 값들을 32비트 자료형인 int형에 세팅. 아두이노 우노에선 int형이 16비트가 할당 됨으로 인		한 오류 발생 및 조치. unsigned long 형으로 데이터 세팅. 블루투스로 라즈베리파이까지 송신할 수 있도록 설		계 

​		Raspberry Pi :   다중 블루투스 입력 구현. 블루투스 검색 함수 구현 도중 너무 많은 블루투스로 인해 속도 문		제 발생 및 해결. 버퍼 문제로 값이 덜 들어오는 현상 디버깅. 호스트가 죽거나, 리소스를 공유할 수 없는경우 		예외처리 생성. 아두이노에서 블루투스로 가져온 데이터 처리 로직 개발. 텍스트 형식의 데이터 누적 및 갱신 		로직 개발.  

​		응용프로그램 초기 출력화면 디자인 구현. 인풋 데이터 존재 가정 후 반복해서 실시간으로 초기화 하는 스레드 		개발. 서버에서 트레픽이 마비될 경우 예외처리 구현하기위한 노력. 딜레이를 통한 동기화 시간 설정.



3일차:

​		Arduino : 변경된 내용을 통한 회로 재설계 및 모듈 제작, 모듈 프로토 타입 치장

​		Raspberry Pi: 디버깅

​		응용프로그램 : 디버깅



4일차:

​		Arduino : 센서간 민감도 조정, 회로 재설계, 모듈 재 제작

​		Raspberry Pi: 디버깅

​		응용프로그램 : 디버깅

​		발표 준비

## ○ 영상

​		

## ○ Code

​		 https://github.com/orgs/OSAMSYR/dashboard 