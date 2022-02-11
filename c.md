# C언어 공부
java 는 객체지향 언어 특징 class  
class c언어에 존재하는 구조체를 기반으로 함

#include <stdio.h> 

int main() 
{
    prinf("Hello, world!\n);
    return 0;
}
<hr/>

1. #include 는 헤더 파일을 포함하는 문법이다
2. printf 함수를 사용하려면 stdio.h(standard input output header file 표준 입출력 파일) 헤더 파일이 필요
3. main은 가장 처음에 실행되는 함수 없으면 실행x
4. return 0; 0이라는 값을 반환, 실행되는 즉시 그 함수는 실행 종료 즉, 현재의 함수에서 빠져 나가라는 의미

### 프로그래밍과 c의 파일 변화
1. 소스 코드 편집 
2. 컴파일
3. 실행 
hello.c -> hello.obj -> hello.exe

### C언어 자료형
* char(1바이트), short(2바이트), int(4바이트), long(4바이트): 정수(저장할 수 있는 크기가 다릅니다)
* float(4바이트), double(8바이트): 실수
* void: 형태가 없는 자료형(포인터를 사용할 때, 함수의 반환값을 표현할 때 등 다양하게 사용됩니다)

### 정수형
* char는 정수와 문자를 표시할 때 사용
* short, int, long, long long은 정수, 즉 숫자를 나타낼 때 사용
* 정수형의 경우 signed(부호 있는 변수), unsigned(부호 없는 변수)로 나뉘어지는데 signed의 경우에는 음수와 양수 둘 다 표현 가능, unsigned의 경우에는 양수만을 표현할 후 있는 대신에 표현 범위가 약 2배 늘어난다 

2022-02-11
인프런 c강의 보는중 Visual Studio로 코딩중이다 