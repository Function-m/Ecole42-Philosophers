# Ecole42-Philosophers

## 목차

1. [프로젝트 개요](#프로젝트-개요)
2. [구현 내용](#구현-내용)
   - [필수 과제](#필수-과제)
   - [보너스 과제 (미구현)](#보너스-과제-미구현)
3. [실행 방법](#실행-방법)
4. [제출 정보](#제출-정보)
5. [참고 자료](#참고-자료)

## 프로젝트 개요

본 프로젝트는 C 언어를 사용하여 철학자들의 식사 문제를 시뮬레이션하는 프로그램입니다.
철학자들은 원탁에 둘러앉아 스파게티를 먹으며, 식사, 생각, 잠의 세 가지 상태를 반복합니다.
각 철학자의 양 옆에 놓여진 포크를 사용하여 식사하며, 포크는 철학자 수만큼 테이블에 놓여 있습니다.
프로그램은 철학자들이 굶어 죽지 않고 식사를 마치도록 관리하며, 각 철학자의 상태 변화를 기록합니다.

## 구현 내용

### 필수 과제

* 각 철학자는 하나의 스레드로 구현됩니다.
* 포크는 각 철학자 사이에 하나씩 존재하며, 뮤텍스를 사용하여 포크의 상태를 보호합니다.
* 프로그램은 다음 인자를 받습니다:
    * `number_of_philosophers`: 철학자의 수 및 포크의 수
    * `time_to_die`: 철학자가 마지막 식사 후 생존 가능한 시간 (밀리초)
    * `time_to_eat`: 철학자가 식사하는 데 걸리는 시간 (밀리초)
    * `time_to_sleep`: 철학자가 잠자는 데 걸리는 시간 (밀리초)
    * `[number_of_times_each_philosopher_must_eat]`: 각 철학자가 식사해야 하는 횟수 (선택 사항)
* 철학자의 상태 변화는 다음 형식으로 기록됩니다:
    * `timestamp_in_ms X has taken a fork`
    * `timestamp_in_ms X is eating`
    * `timestamp_in_ms X is sleeping`
    * `timestamp_in_ms X is thinking`
    * `timestamp_in_ms X died`

### 보너스 과제 (미구현)

* 보너스 과제는 구현하지 않았습니다. 필수 과제만 완료하였습니다.

## 실행 방법

1.  저장소를 클론합니다.
2.  `Makefile`을 사용하여 프로그램을 컴파일합니다.

    ```bash
    make
    ```

3.  다음 형식으로 프로그램을 실행합니다.

    ```bash
    ./philo number_of_philosophers time_to_die time_to_eat time_to_sleep [number_of_times_each_philosopher_must_eat]
    ```

    예시:

    ```bash
    ./philo 5 800 200 500 10
    ```

## 제출 정보

* 제출 디렉토리: `philo/`
* 제출 파일: `Makefile`, `*.h`, `*.c`
* `Makefile` 규칙: `NAME`, `all`, `clean`, `fclean`, `re`

## 참고 자료

* [프로젝트 명세](subject.pdf)
