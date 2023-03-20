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

    $ ./test.sh
    $ sh test.sh
    $ bash test.sh
    
    

