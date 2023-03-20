# day2 - linux 명령어

### pwd
- print working directory의 약자로, 현재 작업 중인 디렉토리의 경로를 반환해주는 명령어입니다.

![pwd](https://user-images.githubusercontent.com/122597068/226290697-d132e298-23c0-43dc-b8b2-5d37cc374fdc.png)

### ls
- list의 약자로, 현재 디렉토리에 속한 파일 및 디렉토리를 나열해줍니다.

|명렁어|기능|
|-----|-----|
| ls | 현재 디렉토리에 있는 내용이 가로 방향으로 출력 |
| ls -a | 숨겨진 파일이나 디렉토리를 출력 (리눅스에서는 파일이름 앞에 .으로 시작하면 숨겨진 파일이란 의미) |
| ls -l | 현재 디렉토리에 있는 자세한 내용을 세로 방향으로 출력(권한,포함된 파일수,소유자,파일크기,수정일자,파일이름) |
| ls -la | 위의 a와 l를 포함한 내용 출력(-la 와 -al은 동일한 명령어) |
|ls -h | K,M,G 단위의 파일 크기를 사용하여 출력 |

![ls](https://user-images.githubusercontent.com/122597068/226292838-048d9c86-7c26-4efb-b824-ec44f28622f9.png)

### chmod
- change mode의 약자로, 파일이나 디렉토리의 퍼미션(허용 권한)을 구정할 수 있는 명령어입니다.
- 제일 앞의 문자 "d"는 디렉토리, "-"는 일반 파일, "i"는 링크를 의미합니다.
- 9자리는 각각 3자리씩 나눠서 권한을 의미합니다.

|첫번째|소유자의 권한|
|두번째|그룹의 권한|
|세번째|other(모든 사용자)에 대한 권한|

- 9자리를 표현하는 문자는 "r","w","x","-" 4가지가 있습니다.
|r|읽기 권한|
|w|쓰기 권한|
|x|실행 권한|
|-|권한 없음|

- rwx는 각각 1비트씩 총 3비트의 공간을 차지합니다.
|r|4|
|w|2|
|x|1|
