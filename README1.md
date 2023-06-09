# day2 - shellscript 문법

### Shell(쉘)이란?

- Shell(쉘)은 운영체제와 사용자 사이를 이어주는 역할을 하며 사용자의 명령어를 해석하고 운영체제가 알아들을 수 있도록 도와주는 명령어 해석기입니다.
- 가장 대표적으로 bash를 사용합니다.


|약어|이름|프롬포트|경로|
|-----|-----|-----|-----|
|bash|Bourne-Again Shell|#|/bin/bash|
|sh|Bourne Shell|$|/bin/sh|
|csh|C Shell|%|/bin/csh|
|ksh|Kron Shell|$|/bin/ksh|
|tcsh|TENEX C Shell|>|/bin/tcsh|

---

### Shell Script(쉘 스트립트)란?
- 운영체제의 Shell을 이용하여 한줄씩 순차적으로 읽으면서 명령어들을 실행시켜주는 프로그램입니다.

---

### 기본

- 스크립트의 최상단에는 `#!/bin/bash` 라는 구문이 있어야 합니다.
- `echo` 혹은 `printf` 로 출력할 수 있습니다.
- 쉘 스크립트 파일을 실행하기 위해서는, 터미널의 파일이 저장된 장소에 가서 아래의 커맨드 중 하나를 선택해서 실행해야 합니다.

<pre>
<code>
 $ ./test.sh
 $ sh test.sh
 $ bash test.sh
 </code>
 </pre>

 - 코드
 
![bin bash](https://user-images.githubusercontent.com/122597068/226344005-543c491b-63a0-4225-92f1-0617a8fe12ea.png)
 
 - 실행결과
 
![bin-bash](https://user-images.githubusercontent.com/122597068/226344094-17db79a7-adc5-4292-b8bd-6f2f53fde283.png)

---

### 변수

- 변수의 이름은 영문자, 숫자, 언더바를 사용할 수 있습니다.
- 변수에 값을 선언할 때는 =의 앞,뒤에 공백 없이 작성해야 하며, 문자열의 경우 쌍따옴표로 감쌉니다.
- 변수를 사용할 때는 앞에 $를 붙여주고, 중괄호를 이용합니다.

---

### 예약변수

- 쉘 스크립트에는 사용자가 정해서 만들 수 없는 이미 정의된 변수가 존재합니다.

|변수|설명|
|-----|-----|
|HOME|사용자 홈 디렉토리를 의미|
|PATH|실행 파일의 경로|
|LANG|프로그램 실행 시 지원되는 언어|
|SHELL|사용자가 로그인시 실행되는 쉘|
|USER|사용자의 계정 이름|
|TERM|로그인 터미널|

- 코드 및 실행결과

![예약변수](https://user-images.githubusercontent.com/122597068/226344162-c8c05f5f-755e-4247-b190-8520c1f165fe.png)

---

### 배열

- 배열 원소는 소괄호안에 공백으로 구분하여 줍니다.
- 배열 안 원소는 문자열이든 정수든 상관 없이 쓸 수 있는 특징이 있습니다.
- 코드 및 실행결과

![배열1](https://user-images.githubusercontent.com/122597068/226344354-e0abe4fb-2cc5-4279-be0d-3a938f23aaee.png)

---

### if문

- if 문의  기본 형식은 다음과 같습니다.
<pre>
<code>
if [ 값1 조건식 값2 ];then

   수행문

 fi
 </code>
 </pre>
- if 문의 조건식 종류는 다음과 같습니다.

|조건식|기능|
|-----|-----|
|-eq|값이 같으면 참|
|-ne|값이 다르면 참|
|-gt|값1 > 값2|
|-ge|값1 >= 값2|
|-lt|값1 < 값2|
|-le|값1 <= 값2|
|-a|&&연산과 동일 and 연산|
|-o|연산과 동일 or 연산|

- if 문의 파일 관련 조건식 종류는 다음과 같습니다.

|조건식|기능|
|-----|-----|
|-d|파일이 디렉토리면 참|
|-e|파일이 있으면 참|
|-L|파일이 심볼릭 링크면 참|
|-s|파일의 크기가 0 보다 크면 참|
|-S|파일 타입이 소켓이면 참|
|-r|파일이 읽기 가능하면 참|
|-w|파일이 쓰기 가능하면 참|
|-x|파일이 실행 가능하면 참|
|파일1 -nt 파일2|파일1이 파일2보다 최신파일이면 참|
|파일1 -ot 파일2|파일1이 파일2보다 이전파일이면 참|
|파일1 -ef 파일2|파일1이 파일2랑 같은 파일이면 참|

- 코드

![if문2](https://user-images.githubusercontent.com/122597068/226344528-96f42eec-e58a-41b6-8d75-feaba4c0551a.png)

- 실행결과

![if문](https://user-images.githubusercontent.com/122597068/226344451-7dbbd204-14c2-4a15-95df-45a6a9ab872d.png)

- 코드

![if문4](https://user-images.githubusercontent.com/122597068/226344685-81ef263d-247a-4f1b-9afb-9b52e97205da.png)

- 실행결과

![if문3](https://user-images.githubusercontent.com/122597068/226344617-b07da8de-75fb-479f-b18d-fd6126c26dca.png)

---

### Switch문
- switch 문의 기본 형식은 다음과 같습니다.
<pre>
<code>
case 변수 in 
	조건・값) 커맨드 ;;
	조건・값) 커맨드 ;;
	조건・값) 커맨드 ;;
esac
 </code>
 </pre>
- 코드

![switch2](https://user-images.githubusercontent.com/122597068/226345157-340c7875-5da6-4c72-a1e4-44f588fc0015.png)

- 실행결과

![swith문](https://user-images.githubusercontent.com/122597068/226344837-6978b654-d1b5-4d79-9002-a0509c2cb923.png)


---

### while문
- while 문의 기본 형식은 다음과 같습니다.
<pre>
<code>
while [ 변수 조건 값 ]
do
	커맨드
done
 </code>
 </pre>
- 코드

![while문2](https://user-images.githubusercontent.com/122597068/226345551-06c4bf9c-8c4c-48c8-bf5a-7a3279cbda46.png)

- 실행결과

![while문](https://user-images.githubusercontent.com/122597068/226345489-904298cd-027f-4009-a6be-6079cc3fffed.png)

---

### for문
- for문의 기본 형식은 다음과 같습니다.
<pre>
<code>
for 변수 in 여러개의 값・변수・범위 
do 
	커맨드 
done
 </code>
 </pre>
 - 코드
 
 ![for문2](https://user-images.githubusercontent.com/122597068/226345367-e9b8185b-661f-4644-9a4b-8e1523fa034b.png)
 
 - 실행결과

![for문](https://user-images.githubusercontent.com/122597068/226345283-d1df6dab-8bf1-4e89-8a90-6927dfe20f7d.png)


---
