### FHS(Fil System Hierarchy Standard)

root

- root directory 이며 최상위 경로이다. / 로 접근이 가능함

/home 

- Home 디렉토리 이외의 다른 디렉토리는 주록 system directory 라고 하는데, 여기선 리눅스 운영과 관리에 관련한 파일들이 존재하는 디렉토리이다.

/bin  & /sbin

- BInary의 약자이며 OS 의 구동을 위해 필요한 프로그램이 들어있는 폴더. cat, chmod, chown, cp, date, echo, kill, ln, ls, mkdir, etx와 같은 기초적 프로그램들이 포함되어 있음
- sbin 폴더는 bin 과 같지만 루트유저 전용 프로그램을 포함한다.

/usr

- user의 약자이며 각 유저 이름에 해당하는 폴더 이름이 존재 각 폴더마다 bin, sbin, shered, lib과 같이 각 유저들이 사용할 수 있는 폴더가 생성되어 있음.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9c0e704-38bb-4011-a47d-e1fa99018cdd/Untitled.png)

### PATH

- / : root 디렉토리
- ~ : home 디렉토리
- 절대경로 Absolute pathsms 이름 그대로 절대적 경로. 경로를 표한하는 방식이 root 디렉토리 부터 시작한다는 점에서 “완전한의 의미에 더욱 가깝다.
- 상대경로 : Relative path 현재 자신의 위치를 기반으로 움직이는 경로
- . : 현재 경로
- .. : 상위 경로
- env : 리눅스의 환경변수를 확인함.

- $PATH
    - 터미널에서 사용하는 명령어의 경로가 저장되어 있음.
    - 여러 경로를 저장하기 위해 각 경로는 : 으로 구분된다.
    

### Configs

- 리눅스에서는 주로 파일을 통하여 설정 (config)
- shell 설정 파일을 비롯한 많은 설정파일들이 대부분 유저의 home 디렉토리에 있음.
- . 으로 시작하는 파일 및 디렉토리는 숨김파일로 간주

(dot file)

- ls 에 a 옵션(all)을 주어야지만 볼 수 있음.
- alias : 일종의 사용자 지정 단축명령어 (.zshrc, .bashrc에 등록)
