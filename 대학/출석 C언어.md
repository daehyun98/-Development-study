프로그램 개발단계
- 프로그램 목적 정의: 요구 분석과 시스템 분석을 통하여 프로그램이 가여야 할 기능 정의
- 프로그램 설계: 분석된 기능을 처리할 수 있도록 프로그램 구조를 설계
- 코드 작성: 프로그램에 대한 설계를 에디터를 사용하여 작성
- 컴파일: 소스코드를 실행 가능한 코드로 변환하고 문법 검사
- 프로그램 실행: 실행 가능한 파일 이름을 입력하여 프로그램 실행
- 테스트와 디버깅: 에러를 검사하고 에러를 디버깅
- 유지보수: 사용 중 발생되는 에러나 추가적인 변경사항을 처리

### C프로그램의 완성 과정
1. 코딩 단계: 주어진 문제에 대한 설계를 바탕으로 소스코드(source code)를 작성하여 소스파일(source file)을 생성하는 과정(c언어 문법으로 이루어짐 .c라는 확장자를 가진 파일로 저장)
2. 컴파일 단계: 소스파일이 목적파일로 변환되는 과정(.c에서 컴파일러를 거치면 .obj로 변환(0과1로 이루어진 파일) )
3. 링킹 단계: 목적파일을 실행파일로 변환하는 과정 (.exe파일)

아스키코드 소문자 a는 97
아스키코드 대문자 A는 65

### 변수 선언 시 고려 사항
- 변수에 저장될 값의 크기 (오버플로우 에러 안뜸)
- 변수의 선언 위치
  - 전역변수
  - 지역변수
- 변수의 초기화

### 선행처리기의 종류와 기능
- #include 파일포함
- #define 매크로 정의
- #if #else #elif #endif 조건부 컴파일

- 주의점
1. 반드시 #로 시작해야 한다
2. 명령문 끝에는 세미크론(;)을 붙이지 않는다
3. 한 줄에 하나의 명령만 쓴다
4. 소스 프로그램의 첫 부분에 위치한다


printf_s() 이렇게 넣어야한다 
vs코드에서는 보안때문에 printf나 scanf 안됌


선택/반복 제어문
- 


### 과제

#define _CRT_SECURE_NO_WARNINGS  // scanf 보안 경고로 인한 컴파일 에러 방지
#include <stdio.h> //  표준입출력에 관한 함수들이 정의되어 있는 헤더파일을 포함한다

int main(void) //메인함수가 인자값을 받지 않는다,함수의 반환값이 정수형이다
{
    int Jumsu;  // 정수형 자료형으로 변수 Jusmsu 선언

    printf("0점에서 100점수 사이의 점수를 입력하세요. \n"); //printf 출력함수, \n 줄바꿈(이스케이프 시퀀스) 
    scanf("%d", &Jumsu);  //표준 입력(키보드)을 받아 변수Jumsu 에 값을 저장

    if (Jumsu >= 0 && Jumsu < 60)  //조건연산 Jumsu가 0보다 크거나 같고 60미만이면 F학점 &&논리곱(양쪽 모두 참일 때만 참)
        printf("%d점은 F학점입니다.\n", Jumsu); //scanf로 입력을 받아 조건문으로 검사해서 출력하고 줄바꿈 

    else if (Jumsu >= 60 && Jumsu < 70) // Jumsu가 60보다 크거나 같고 70미만이면 D학점
        printf("%d점은 D학점입니다.\n", Jumsu);

    else if (Jumsu >= 70 && Jumsu < 80) // Jumsu가 70보다 크거나 같고 80미만이면 C학점
        printf("%d점은 C학점입니다.\n", Jumsu);

    else if (Jumsu >= 80 && Jumsu < 90) // Jumsu가 80보다 크거나 같고 90미만이면 B학점
        printf("%d점은 B학점입니다.\n", Jumsu);

    else if (Jumsu >= 90 && Jumsu <= 100) // Jumsu가 90보다 크거나 같고 100미만이거나 같으면 A학점
        printf("%d점은 A학점입니다.\n", Jumsu);

    return 0; //반환값으로 0을 반환, 0을 반환하면 함수 종료
}

- 스위치문으로 변환
#include <stdio.h> //표준입출력에 관한 함수들이 정의되어 있는 헤더파일을 포함한다


int main(void) //메인함수가 인자값을 받지 않는다,함수의 반환값이 정수형이다
{
	int Jumsu; // 정수형 자료형으로 변수 Jusmsu 선언

	printf("0점에서 100점수 사이의 점수를 입력하세요.\n"); //printf 출력함수, \n 줄바꿈(이스케이프 시퀀스) 
	scanf_s("%d", &Jumsu);  //표준 입력(키보드)을 받아 변수Jumsu 에 값을 저장

	switch (Jumsu/10) //점수를 10으로 나눈다 
	{
	case 6: //(Jumsu > 60 && Jumsu < 70);    60을 10으로 나눠도 6이 나온다 60~69까지
		printf("%d점은 D학점입니다.\n", Jumsu); 
		break; //case중 해당하면 아래 코드를 전부 실행시키기 때문에 break을 써서 원하는 코드만 실행시키고 switch문 종료를 시켜야함
	case 7: //(Jumsu > 70 && Jumsu < 80);   70을 10으로 나눠도 7이 나온다 70~79까지
		printf("%d점은 C학점입니다.\n", Jumsu);
		break;
	case 8: //(Jumsu > 80 && Jumsu < 90);   80을 10으로 나눠도 8이 나온다 80~89까지
		printf("%d점은 B학점입니다.\n", Jumsu);
		break;
	case 9: case 10:  //(Jumsu > 90 && Jumsu <= 100); case 9만 있으면 100은 A로 안나오니 case10까지 같이 썼다
		printf("%d점은 A학점입니다.\n", Jumsu);
		break;
	default: //60점 미만은 default로 나오게 작성했다     
		printf("%d점은 F학점입니다.\n", Jumsu);
	}
	return 0; //반환값으로 0을 반환, 0을 반환하면 함수 종료
}



- 과제 2
#include <stdio.h>

void main(void)
{
	int num = 0;
	int odd_total_num = 0;
	int even_total_num = 0;
	printf("1~100 사이 숫자를 입력 하세요 : \n");
	scanf_s("%d", &num);
	if (num <= 100) {
		for (num; num >= 1; num--) {
			if (num % 2 == 1) {
				odd_total_num = odd_total_num + num;
			}
			else if (num % 2 == 0) {
				even_total_num = even_total_num + num;
			}
		}
		printf("홀수 값의 총 합계 : %d \n", odd_total_num);
		printf("짝수 값의 총 합계 : %d \n", even_total_num);
	}
	else {
		printf("입력값이 100이 넘습니다\n");
	}
}

- while로 바꿈
#include <stdio.h>  //표준입출력에 관한 함수들이 정의되어 있는 헤더파일을 포함한다
void main(void) //main() 함수가 종료할때 아무 값도 리턴하지 않겠다는 뜻
{
	int num = 0; //정수형 자료형으로 변수 num 선언하고 초기화
	int odd_total_num = 0; //정수형 자료형으로 변수 odd_total_num 선언하고 초기화
	int even_total_num = 0; //정수형 자료형으로 변수 even_total_num 선언하고 초기화
	printf("1~100 사이 숫자를 입력 하세요 : \n"); //printf 출력함수
	scanf_s("%d", &num); //표준 입력(키보드)을 받아 변수 num에 값을 저장
	if (num <= 100) { //만약 num보다 크고 100미만이거나 같으면
		while (num != 0) { //반복제어문 scanf_s로 받아, 0이 아니면 계속 반복
			num >= 1; // num이 1보다 크거나 같으면
			num--; //num은 하나씩 빼준다
			if (num % 2 == 1) { //만약에 num이 홀수면
				odd_total_num = odd_total_num + num; //조건문 출력 total에 num 더함
			}
			else if (num % 2 == 0) { //만약에 num이 짝수면
				even_total_num = even_total_num + num;//조건문 출력 total에 num 더함
			}
		}
		printf("홀수 값의 총 합계 : %d \n", odd_total_num); //출력
		printf("짝수 값의 총 합계 : %d \n", even_total_num);//출력
	}
	else { //입력값이 100이 넘으면 출력
 		printf("입력값이 100이 넘습니다\n");
	}
}

2022-04-14
출석수업 과제물 제출