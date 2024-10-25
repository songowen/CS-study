# 기본 컴퓨터 구조

**컴퓨터 구조(Computer Architecture)**는 컴퓨터 시스템이 어떻게 구성되고 동작하는지를 설명하는 분야입니다. 컴퓨터의 성능과 효율성을 결정짓는 핵심적인 요소들을 다룹니다.

<details>
<summary>Table of Contents</summary>

- [RDBMS의 기본](#컴퓨터가-이해하는-정보)
- [SQL](#cpu)
- [효율적 쿼리](#메모리)
- [데이터베이스 설계](#보조-기억장치와-입출력-장치)
- [NOSQL](#보조-기억장치와-입출력-장치)

</details>

---

# 컴퓨터 구조 개념

## 컴퓨터가 이해하는 정보

컴퓨터는 0과 1로 이루어진 이진법을 사용하여 정보를 처리합니다. 이러한 정보를 **비트(Bit)**라고 하며, 8비트는 1바이트(Byte)를 구성합니다. 컴퓨터는 모든 데이터를 이진법으로 변환하여 처리합니다.

### CPU(중앙 처리 장치)

컴퓨터의 두뇌 역할을 하며, 명령어를 해석하고 실행합니다.
산술 연산과 논리 연산을 수행하고, 메모리에서 데이터를 읽거나 기록하는 작업을 관리합니다.
CPU는 일반적으로 ALU(산술 논리 장치), 제어 장치, 레지스터 등으로 구성됩니다.

### 메모리

**메인 메모리(RAM)**는 데이터를 일시적으로 저장하는 장치로, CPU가 빠르게 접근할 수 있습니다.
메모리는 프로그램 실행 중에 데이터를 저장하고 불러오는 역할을 합니다.
RAM은 휘발성 메모리로, 전원이 꺼지면 데이터가 사라집니다.

### 보조 기억장치

HDD나 SSD와 같은 저장 장치로, 데이터를 영구적으로 저장합니다.
속도는 메인 메모리보다 느리지만 대용량 데이터를 저장할 수 있습니다.

### 버스(Bus)

CPU, 메모리, 입출력 장치 간의 데이터를 주고받는 통로입니다.
데이터 버스, 주소 버스, 제어 버스로 나뉘며, 각각의 역할에 따라 데이터를 효율적으로 전달합니다.

### 입출력 장치(I/O Devices)

키보드, 마우스, 모니터, 프린터 등 외부 장치들과 컴퓨터 간의 상호작용을 담당합니다.
사용자와 컴퓨터가 정보를 주고받을 수 있도록 도와줍니다.
이러한 컴퓨터 구조의 구성 요소들은 서로 협력하여 컴퓨터 시스템이 작동하게 합니다. CPU는 메모리와 입출력 장치와 상호작용하며, 데이터를 처리하고 명령을 실행하여 사용자가 원하는 작업을 수행합니다

## CPU

**중앙 처리 장치(CPU, Central Processing Unit)**는 컴퓨터의 두뇌로, 명령을 해석하고 실행하는 역할을 합니다. CPU는 산술 연산을 수행하고, 메모리에서 데이터를 불러와 명령을 처리하는 역할을 합니다.

## 메모리

**메모리**는 데이터를 임시로 저장하는 공간입니다. 메모리는 크게 휘발성 메모리(RAM)와 비휘발성 메모리로 나뉩니다. RAM은 컴퓨터가 켜져 있을 때만 데이터를 유지하며, 컴퓨터가 꺼지면 데이터가 사라집니다.

## 보조 기억장치와 입출력 장치

**보조 기억장치**는 데이터를 영구적으로 저장하는 장치로, 대표적으로 하드 디스크(HDD)와 SSD가 있습니다. **입출력 장치**는 컴퓨터와 외부 세계 간의 정보를 주고받는 장치로, 키보드, 마우스, 모니터, 프린터 등이 포함됩니다.


# 컴퓨터가 이해하는 정보

## 데이터

### 비트

- 0과 1을 나타내는 가장 작은 정보단위
- N비트는 2^N(제곱)의 정보를 표현

### 바이트

- 큰 단위들은 byte, kB, MB, GB, TB로 표현
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/9ae3041b-6e73-491c-b757-10260e6073e0/image.png)
    

### 워드

- CPU가 한번에 처리할 수 있는 데이터 크기
    - 위 단위(kB, MB, GB, TB)들은 프로그램 관점의 정보단위
- 현대 컴퓨터 대부분의 워드 크기는 32비트 혹은 64비트

### 숫자표현법

- 정수
    - CPU는 0과 1만을 이해할 수 있음(2진법)
    - 1을 넘어가는 시점에서 자리올림
    - 컴퓨터가 이해하는 정보를 표현할 때 16진수도 사용함
- 소수
    - 부동소수점 표현방식
        - 0.1 + 0.2 ≠ 0.3 → ?????
    - 지수와 가수
        - 1.1011 * 2^N에서 1.1011은 가수, N은 지수
        - 가수의 경우 **1로 고정한 후** 지수를 조절함
            - ex)1101101.11 * 2^0 →1.10110111 * 2^6
    - 10진수의 소수를 2진수로 표현할때 소수의 표현이 딱 맞아 떨어지지 않음
        - ex) 1/3을 10진수와 3진수로 표현
            - → 1 * 3^-1
            - → 0.333333333……

### 문자표현법

- 문자인코딩
    - 문자를 0과 1로 이루어진 문자코드로 변환
- 문자디코딩
    - 0과 1로 표현된 문자코드를 문자로 변환
- 아스키 문자
    - 8비트(1바이트)의 용량을 지님
    - 1비트는 오류검출을 위해 사용(패리티비트)
    - 7비트 → 128개의 문자를 표현
- EUC-KR
    - 16비트(2바이트)의 용량
    - 2350개의 한글 단어 표현, 모든한글조합 X
        - 쀓, 똠과 같은 글자는 EUC-K 표현 불가능
        - 아스키 코드와 EUC-KR(사진)
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/148fd9bc-a549-4c46-84da-cdcc384a8a02/image.png)
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/c22e3995-36ea-49dd-9969-6292634d4eed/image.png)
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/f9bbab9f-7017-4fd9-bf5c-14ad1ed01a9f/image.png)
            
- 유니코드
    - 통일된 문자 집합
    - 대부분 언어 지원
    - 가장 많이 사용되는 표준 문자 집합
    - 문자에 부여된 값을 인코딩하는 방식
        - UTF-8, UTF-16, UTF-32
- base64
    - 이진데이터까지 변환할 수 있는 인코딩 방식
    - 나누어 떨어지지 않는 자리는 패딩이 되고 ‘=’으로 인코딩 됨
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/38f3965a-eb20-434e-b91f-9ad9283ab386/image.png)
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/c8685619-9584-4457-ac84-3e83774d27fc/image.png)
        

## 명령어

- 수행할 대상 → 데이터 자체 or 데이터가 저장된 위치

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/68ba28b2-67f3-446b-bbdd-a1026c03907f/image.png)

- 동작 → 연산코드(opercode)
    - 데이터 전송, 산술/논리연산, 제어 흐름 변경, 입출력 제어 등이 있음
- 대상 → 오퍼랜드(operand)
    - 메모리 주소나 레지스터 이름이 명시됨 → 주소필드라고 불림

### 어셈블리어

- 0과 1로 표현된 기계어를 읽기 편한 형태로 단순 번역한 언어
- ex) 어떤 수의 제곱을 반환하는 함수
    - C
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/add8532a-f970-4024-aff8-14368bbf37c5/image.png)
        
    - CISC기반 CPU 어셈블리어
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/09909ed8-a336-4303-b4de-2281d4508334/image.png)
        

### 명령어 사이클

- 프로그램 속 명령여들이 반복하여 실행되는 일정한 주기
- 인출 사이클(fetch cycle)
    - 메모리에 있는 명령어를 CPU로 가져오는 단계
- 실행 사이클(execution cycle)
    - CPU로 가져온 명령어를 실행하는 단계
- 간접 사이클(indirect cycle)
    - 데이터의 주소가 명시된 경우 한번 더 메모리에 접근하는 단계
- 인터럽트 사이클 → CPU레지스터 학습 필요

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/f2116f0a-cb6d-490a-a306-bab7cbcd678f/image.png)

# CPU

## 레지스터

- CPU 안에 있는 임시 저장장치
- 다양한 레지스터들이 각기 다른 **이름과 역할**이 있음
- 하위 항목에 있는 레지스터들은 대부분의 CPU가 공통적으로 포함하고 있는 대표적 주요 레지스터

### 프로그램 카운터(PC, Program Counter)

- 메모리에서 다음으로 읽어들일 명령어의 주소를 저장
    - 이를 **명령어 포인터(IP, Instruction Pointer)**라고 부르는 CPU도 있음

### 명령어 레지스터(IR, Instruction Register)

- **해석할 명령어**(메모리에서 읽어들인 명령어)를 저장하는 레지스터
- CPU내의 제어장치는 명령어 레지스터 속 명령어를 해석하게 됨

### 범용 레지스터(general purpose reister)

- 다양하고 일반적인 상황에서 자유롭게 사용할 수 있는 레지스터
- 데이터, 명령어, 주소 모두 저장할 수 있음
- 일반적으로 CPU에 여러개의 범용 레지스터들이 있음

### 플래그 레지스터(flag register)

- 연산의 결과 혹은 CPU 상태에 대한 부가정보인 **플래그** 값을 저장하는 레지스터
    - 플래그 : CPU가 명령어를 처리하는 과정에서 반드시 참조해야 할 상태 정보
    - 대표적인 플래그
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/43830930-6998-4ed8-9586-ed487ec18223/image.png)
        

### 스택 포인터(stack pointer)

- 메모리의 스택영역에서 최상단 스택 데이터 위치를 가리키는 레지스터
- 밑의 그림에서 스택 데이터 3이 저장된 주소를 가리키고 있음
    - 이때 스택 데이터 3을 꺼내게 된다면, 스택 데이터 2가 저장된 주소를 가리키게 됨

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/5d3137a7-b496-4da3-9a00-a1326db775c0/image.png)

## 인터럽트

- CPU의 작업을 방해하는 신호
- 크게 동기 인터럽트와 비동기 인터럽트로 나뉨
    - 동기 인터럽트
        - CPU가 프로그래밍 오류와 같은 예외적인 상황을 마주쳤을 때 발생하는 인터럽트
        - 예외(exception)이라고도 불림
    - 비동기 인터럽트
        - 입출력 장치에 의해 발생하는 인터럽트
        - 세탁기의 세탁완료 알림, 전자레인지의 조리 완료 알림과 같은 **알림**의 역할을 함
            - ex1) CPU가 프린터와 같은 입출력장치에게 입출력 작업을 명령하고, 이후 작업이 끝난 입출력장치가 CPU로 **완료 알림(인터럽트)**을 보낸다
            - ex2) 키보드, 마우스와 같은 입출력장치가 어떤 입력을 받아들였을 때, 이를 처리하기 위해 CPU에 **입력** **알림(인터럽트)**을 보낸다
- 일반적으로 인터럽트라 부르는 것은 비동기 인터럽트를 말하는 것
    - (여기서는 비동기 인터럽트를 구분하기 위해 하드웨어 인터럽트라 칭함)

### 하드웨어 인터럽트

- 효율적으로 명령어를 처리하기 위해 사용
    - CPU가 한 작업에 대기하는 것보다, 완료 알림이 올 때 까지 다른 작업을 처리함
- CPU가 하드웨어 인터럽트를 처리하는 순서 (일반적으로)
    1. 입출력 장치가 CPU에 **인터럽트 요청 신호**를 보냄
    2. CPU는 실행 사이클이 끝나고 명령어를 인출하기 전에 항상 인터럽트 여부를 확인함
    3. CPU는 인터럽트 요청을 확인하고, **인터럽트 플래그**를 통해 현재 인터럽트를 받아들일 수 있는지 여부를 확인함
    4. 인터럽트를 받아들일 수 있다면 CPU가 지금까지의 작업을 백업함
    5. CPU는 **인터럽트 벡터**를 참조하여 **인터럽트 서비스 루틴**을 실행
    6. 인터럽트 서비스 루틴 실행이 끝나면 4. 에서 백업해 둔 작업을 복구하여 실행 재개
- **인터럽트 요청 신호**
    - CPU에 인터럽트 가능 여부를 확인하기 위한 신호
- **인터럽트 플래그**
    - 인터럽트 요청 신호를 수용할지, 무시할지 결정하는 플래그
    - 여기서 인터럽트 플래그가 불가능으로 설정되어 있다면 인터럽트 요청이 오더라도 요청을 무시함
        - 이 때 하드웨어 고장이나, 정전으로 인한 인터럽트등과 같이 막을 수 없는 인터럽트도 있음
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/210790ea-dc2c-43b9-a6ac-073da86c1c7b/image.png)
            
- **인터럽트 서비스 루틴**
    - 인터럽트를 어떻게 처리하고 작동해야 할 지에 대한 정보로 이루어진 프로그램
    - CPU는 인터럽트 서비스 루틴을 실행하고, 본래 작업으로 다시 돌아가야 함
    - 입출력장치마다 각기 다른 인터럽트 서비스 루틴을 가지고 있음
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/eac31d5e-add9-4642-826a-499a6e352fb3/image.png)
        
- **인터럽트 벡터**
    - 메모리에 저장되어 있는 인터럽트 서비스 루틴들을 식별하기 위한 정보
        - 인터럽트 서비스 루틴의 시작주소 가지고 있음
    - 인터럽트 서비스 루틴을 실행시키기 위해 필요
- 해당 인터럽트를 처리하기 위해서 지금까지의 작업들은 인터럽트 서비스 루틴을 실행하기 전, 현재 프로그램을 재개하기 위해 필요한 모든 내용을 **메모리 내 스택에 백업**

- 위의 메모리 사이클(컴퓨터가 이해하는 정보/명령어/명령어 사이클)에 인터럽트 사이클을 추가한 모습
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/2a67d2cf-5d5e-4094-a8b2-2d700482f66e/image.png)
    

### 예외

- 폴트, 트랩, 중단, 소프트웨어 인터럽트 등이 있음
- 예외 발생 시 작업을 중단 후 해당 예외 처리, 예외 처리 후 작업 재개

- **폴트 fault**
    - **예외가 발생한 명령어부터** 실행을 재개하는 예외
- **트랩 trap**
    - **예외가 발생한 명령어의 다음 명령어부터** 실행을 재개하는 예외
- **중단 abort**
    - **프로그램을 강제로 중단** 시킬 수 밖에 없는 심각한 오류를 발견했을 때 발생하는 예외
- **소프트웨어 인터럽트**
    - 시스템 콜이 발생했을 때 발생하는 예외 (3장에서 학습 예정)

## CPU 성능 향상을 위한 설계

### CPU 클럭 속도

- **클럭**
    - 컴퓨터 부품을 일사불란하게 움직일 수 있게 하는 **시간의 단위**
- **클럭 속도**
    - 헤르츠(Hz) 단위로 측정 : 1초에 몇번 반복되는지 나타내는 단위
    - 최근에는 클럭 속도가 매우 빨라져, 기가헤르츠(GHz) 단위로 측정하는 것이 일반적
    - CPU의 속도 단위로 간주됨
        - 필요 이상으로 높이면 **발열**이 심해지기 때문에, 클럭 속도로 성능을 높이기엔 **한계**가 있음

### 멀티코어와 멀티스레드

- 클럭 속도를 높이는 방법 이외에 CPU성능을 높이는 방법
- **코어**
    - CPU에서 명령어를 읽어들이고, 해석하고, 실행하는 부품
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/29316cea-2310-4f8a-80a0-a2d7b2ca9bc9/image.png)
        
- **스레드**
    - **하드웨어 스레드(CPU)**
        - 하나의 코어가 동시에 처리하는 명령어 단위
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/14733761-7a7e-44ad-b7c1-49934275a36d/image.png)
            
        - **논리 프로세서**라고도 불림
    - **소프트웨어 스레드(프로그램, 운영체제)**
        - 하나의 프로그램에서 독립적으로 실행되는 단위
        - 예시
            
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/20e44cab-07c9-48f9-8e4e-4bcce52b0d8c/image.png)
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/8f6ab77e-ce6c-46df-90d1-de9ae1f70fb5/image.png)
            
    - **병렬성과 동시성**
        - **병렬성** : 작업을 물리적으로 **동시에 처리하는** 성질 (하드웨어 스레드)
        - **동시성** : 작업을 **동시에 처리하는 것처럼** 보이려는 성질 (소프트웨어 스레드)
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/46d4292c-1566-43ba-a2a6-186a7f2c9751/image.png)
            
- CPU 클럭 속도와 코어, 멀티스레드(논리 프로세서)는 다음과 같이 확인됨
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/1d454c60-62d8-4a88-b367-72f919dc8049/image.png)
    

## 파이프라이닝을 통한 명령어 병렬 처리

- 명령어 병렬 처리 기법
    - CPU를 한시도 쉬지않고 작동시킴으로써 CPU의 성능을 높이는 기법
    - 현대 CPU 명령어 처리에서 절대 빠질 수 없는 핵심기술

### 명령어 파이프라인

- 명령어 처리과정
    1. 명령어 인출
    2. 명령어 해석
    3. 명령어 실행
    4. 결과 저장
    - 같은 단계가 겹치지 않는다면 동시에 실행할 수 있음
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/9a2aeab9-3cf7-4c8a-b194-6466c2c1d966/image.png)
        

### CISC(Complex Instruction Set Computer)

- 인텔 x86 or x86-64 CPU
- 복잡한 명령어 집합
- 적은 수의 명령어로 프로그램 실행

### RISC(Reduced Instruction Set Computer)

- 애플 M1 CPU
- CISC 에 비해 활용 가능한 명령어 종류 적음
- 짧고 규격화된 명령어
- 1클럭 내외로 실행되는 명령어 지향
- CISC는 RISC에 비해 명령어 수행시간이 길고 들쑥날쑥 하기 때문에 파이프라이닝에 비효율적일 수 있음
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/818d5065-8406-43c6-afb6-fdd05366918e/image.png)
    

### 파이프라인 위험pipline hazard

- 파이프라이닝이 CPU 성능 향상에 실패하는 경우
- **데이터 위험**
    - 명령어간의 데이터 의존성
    - ex) 명령어 2가 명령어 1에 의존적인 경우, 명령어 1이 끝나기 전까지 명령어 2 인출 불가능
- **제어위험**
    - 프로그램 카운터의 갑작스러운 변화
    - 프로그램 카운터는 (기본적으로)현재 실행중인 명령어의 다음 주소로 갱신이 됨
        - 이때 JUMP, 인터럽트 등으로 인해 명령어 프로그램 실행 흐름이 바뀐다면, 미리 인출 or 해석중인 명령어 쓸모x
- **구조적 위험**
    - 서로 다른 명령어가 동시에 ALU, 레지스터 등 같은 CPU 부품을 사용하려고 할 때 발생
    - 자원 위험이라고도 부름

# 메모리

## RAM

- 임의 접근 메모리
    - 임의접근 : 저장된 요소에 순차적으로 접근할 필요 없이 임의의 위치에 곧장 접근 가능한 방식
        - 직접 접근이라고도 부름
    - 순차접근은 임의접근에 반대되는 개념
        - 특정 위치에 저장된 요소에 접근하기 위해서 순차적으로 접근하는 방식

### RAM의 종류

1. DRAM(Dynamic RAM)
    - 시간이 지나면 저장된 데이터가 점차 사라지는 RAM
2. SRAM(Static RAM)
    - 시간이 지나도 저장된 데이터가 사라지지 않는 RAM
3. SDRAM(Synchronous Dynamic RAM)
    - 클럭 신호와 동기화된 발전된 형태의 DRAM
4. DDR SDRAM(Double Data Rate SDRAM)
    - 대역폭을 넓혀 속도를 빠르게 만든 SDRAM
        - 대역폭 : 데이터를 주고받을 길의 너비
    - SDRAM에 너비가 두배
    - DDR 뒤의 숫자(DDR2, DDR3 …)은 이전 숫자에 비해 대역폭이 두 배 넓다는 것을 의미함

## 메모리에 바이트를 밀어넣는 순서

- 메모리는 CPU로 부터 데이터를 워드 단위(4바이트, or 8바이트)로 받아들임
- 하지만 메모리는 데이터를 1바이트 단위로 저장하고 관리함
- 해당 데이터를 쪼개어 여러주소에 걸쳐 저장해야함

### 빅 엔디안

- 낮은 번지 주소에 상위 바이트부터 저장하는 방식
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/3b791e12-2e57-4f31-841d-3c1a62ffc739/image.png)
    
- 메모리 값을 직접 읽거나 디버깅할 때 편리함

### 리틀 엔디안

- 낮은 번지 주소에 하위 바이트부터 저장하는 방식
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/7dbd0369-aa97-4f78-b127-98aa3b14dd4b/image.png)
    
- 메모리 값을 직접 일고 쓰기는 불편하지만, 수치계산이 편리함

## 캐시 메모리

- CPU의 연산 속도와 메모리 접근 속도의 차이를 줄이기 위해 탄생한 저장장치
- CPU와 메모리 사이에 위치한 SRAM 기반의 저장장치
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/45ae2317-b4cb-43d5-8843-9967bd797bc4/image.png)
    
- 코어와 가장 가까운 순서대로 **L1캐시, L2캐시, L3캐시**로 불림
    - 이중 L1과 L2 캐시는 코어 내부에, L3는 코어 외부에 위치함
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/7427c8bf-5c34-4b7a-8f7e-604dfde7e021/image.png)
    
- 캐시 메모리의 속도는 L1, L2, L3 순으로 빠르고, 크기는 L3, L2, L1 순으로 큼
- 해당 메모리 크기는 작업관리자에서 확인 가능함

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/bffa8c56-a697-46a1-9d27-64fc44332c38/image.png)

- 멀티코어인 경우는 L1, L2는 코어마다 위치, L3는 여러 코어가 공유하는 형태
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/5bcbb3e9-d834-417c-8852-86450f9af2c0/image.png)
    
- L1 캐시 메모리는 명령어만을 저장하는 L1l캐시와 데이터만을 저장하는 L1D캐시로 구분하기도 함(**분리형 캐시**)
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/624fbc4f-14e4-4cc6-901a-ac2c9c505a35/image.png)
    

### 캐시 히트와 캐시 미스

- 캐시메모리는 CPU가 사용할 법한 것을 저장
- 예측하여 저장한 데이터가 실제로 사용되는 경우 → 캐시히트
- 틀린 예측으로 인해 CPU가 메모리로부터 필요한 데이터를 직접 가져와야 하는 경우 → 캐시미스
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/bcc1742b-8772-455c-913f-a5790ea780c5/image.png)
    

### 참조 지역성의 원리

- 캐시 메모리가 메모리로 부터 가져올 데이터를 정하게 하는 특정한 원칙
- 시간 지역성, 공간지 역성이 있음
- 시간 지역성
    - 최근에 접근했던 메모리 공간에 다시 접근하려는 경향
    - ex) 프로그래밍 언어의 **변수**
- 공간 지역성
    - 접근한 메모리 공간의 근처에 접근하려는 경향
    - ex) 배열(array)

### 캐시 메모리 쓰기 정책의 일관성

1. 즉시쓰기
    - 메모리를 항상 최신상태로 유지
    - 버스 사용시간이 늘어남
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/18791f59-73ce-4bfe-8496-3239fa7f91de/image.png)
        
2. 지연 쓰기
    - 캐시 메모리에만 값을 써 두었다가 추후 수정된 데이터를 한번에 메모리에 반영하는 방법
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/96139cb9-90a7-4f27-9cfa-5c88a854870c/image.png)
    

# 보조기억장치와 입출력장치

- 보조기억장치
    - 하드디스크 드라이브
    - 플래시 메모리 기반 저장장치
        - SSD
    - 전원이 꺼져도 데이터를 안전하게 보관
    - CPU가 필요로 하는 정보를 조금이라도 빠른 성능으로 메모리에 전달

## RAID

- **데이터의 안정성** 혹은 **성능**을 확보하기 위해 **하나의 보조장치처럼 사용**하는 기술
- RAID를 구성하는 방법은 여러가지, **RAID레벨**이라고 표현

### RAID0

- 데이터를 보조장치에 단순하게 나누어 저장하여 구성하는 방식
- 줄무니처럼 분산되어 저장하는 동작을 스트라이핑이라고 함
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/8ebc7e3a-b69c-4eff-8bb2-99d12a5ecc39/image.png)
    
- 장점 : 빠른 입출력 속도
- 단점 : 저장된 정보 안전하지 않음

### RAID1

- 완전한 복사본을 만들어 저장하는 구성 방식
    - 미러링이라고도 불림
- 장점 : 복구가 간단하고 안정성이 높음
- 단점 : 사용 가능한 용량이 적어짐
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/52df180c-4395-49f3-bb5f-495d6b94ff45/image.png)
    

### RAID4

- 패리티 정보를 저장하는 디스크를 따로 두는 구성방식
    - 패리티 → 오류를 검출할 수 있는 정보
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/c51236ab-8381-4faa-8744-e6ac224f0f20/image.png)
    
- 장점 : RAID1에 비해 적은 하드디스크로도 안전하게 데이터 보관
- 단점 : 패리티를 저장하는 장치에 병목 현상 발생

### RAID5

- 패리티를 분산하여 저장하는 구성방식
- RAID4의 병목현상 보완 가능
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/fdfa74ed-9093-49f5-b50e-a7ea9aba0d3f/image.png)
    

### RAID6

- 기본 구성은 RAID5와 같지만 서로 다른 2개의 패리티를 두는 구성방식
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/82d13ec2-6db3-4531-af71-dc65988f4127/image.png)
    
- 장점 : RAID4 나 RAID5에 비해 안정성이 높음
    - 오류를 검출하고 복구할 수 있는 수단이 2개가 생기기 때문
- 단점 : RAID5에 비해 쓰기 속도는 느림
    - 새로운 정보를 저장할 때 마다 함께 저장할 패리티가 2개 생기기 때문에

## 입출력 기법

### 장치 컨트롤러

- CPU와 입출력장치 사이의 통신을 중개하는 역할의 하드웨어

### 장치 드라이버

- 장치 컨트롤러의 동작을 알고, 장치 컨트롤러가 컴퓨터 내부와 정보를 주고 받을 수 있도록 하는 프로그램

### 프로그램 입출력

- 프로그램속 명령어로 입출력 작업을 수행하는 방법

### 인터럽트 기반 입출력 - 다중 인터럽트

- 인터럽트가 여러 입출력 장치로부터 동시 다발적으로 발생하는 경우
    - 우선순위가 더 높은 인터럽트가 우선적으로 처리됨
    - 이미지
        - 일반적인 흐름
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/f1aaefad-143d-43f8-8eed-d97d7e38173c/image.png)
            
        - 인터럽트A의 서비스 루틴 중 인터럽트 B 요청이 들어올 경우
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/0deefb7e-e24b-455d-bed0-c4e4f97f1999/image.png)
            
- 프로그래머블 인터럽트 컨트롤러(이하 PIC) →다중 인터럽트를 처리하기 위한 하드웨어
    - 하드웨어 인터럽트 요청들의 우선순위를 판별한 뒤, CPU에게 지금 처리해야 할 하드웨어 인터럽트가 무엇인지를 알려주는 장치
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/13f468a7-76a3-4ede-8e64-d7add92fa8b8/image.png)
        

### DMA 입출력

- 직접 메모리에 접근할 수 있는 입출력 기능
- 시스템 버스에 연결된 DMA 컨트롤러라는 하드웨어 필요
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/0b643064-1102-4701-b27c-d3bdda30dfd7/image.png)
    
- PCIe
    - 오늘날 메인보드에서 가장 대중적으로 볼 수 있는 입출력 버스
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/61a3c15c-c245-4a29-8115-ac9b8fced4e1/image.png)
        
    - 버전이 존재
        - 버전에 따른 속도 표
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c0694fc7-45ff-4378-aee7-a1e395ff302c/6dacfaab-7d21-4c28-a2c0-bf0489a7e0c6/image.png)
            
    - 레인
        - PCIe 버스를 통해 정보를 송수신하는 단위
        - 개수가 2개, 4개 , 8개가 되면 한번에 통신을 주고받을 수 있는 양도 2배, 4배, 8배가 됨