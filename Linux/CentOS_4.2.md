# 리눅스 기본 명령어

### ls
List의 약자로 Windows의 'dir'과 같은 역할을 한다. 즉, 해당 디렉터리(=폴더)에 있는 파일의 목록을 나열한다.

> - [사용 예]
> - ls : 현재 디렉터리의 파일 목록
> - ls /etc/sysconfig : /etc/sysconfig 디렉터리의 목록
> - ls -a : 현재 디렉터리의 목록(숨김 파일 포함)
> - ls -l : 현재 디렉터리의 목록을 자세히 보여줌

### cd
Change Directory의 약자로 디렉터리를 이동하는 명령이다.

> - [사용 예]
> - cd : 현재 사용자의 홈 디렉터리로 이동
> - cd ~centos : centos 사용자의 홈 디렉터리로 이동
> - cd .. : 바로 상위의 디렉터리로 이동.(".."은 현 디렉터리의 부모 디렉터리를 의미)
> - cd /etc/sysconfig : /etc/sysconfig 디렉터리로 이동(절대 경로)
> - cd ../etc/sysconfig : 상대 경로로 이동.

### pwd
print Working Directory의 약자로 현재 디렉터리의 전체 경로를 화면에 보여준다.
#### cd 명령어로 디렉터리를 이동 후에는 바로  pwd 명령어로 현재 디렉터리를 확인하는 습관을 가지자.

### rm
ReMove의 약자로 파일이나 디렉터리를 삭제한다.

> - [사용 예]
> - rm abc.txt : 해당 파일을 삭제(내부적으로 'rm -i'로 연결됨)
> - rm -i abc.txt : 삭제 시 정말 삭제할지 확인하는 메시지가 나옴
> - rm -f abc.txt : 삭제 시 확인하지 않고 바로 삭제
> - rm -r abc : 해당 디렉터리를 삭제(r은 Recursive의 약자이다.)
> - rm -rf abc : 해당 디렉터리와 그 아래에 있는 하위 디렉터리를 강제로 전부 삭제

### cp
CoPy의 약자로 파일이나 디렉터리를 복사한다. 새로 복사한 파일은 복사한 사용자의 소유자가 된다. 그러므로 명령어를 실행하는 사용자는 해당 파일의 읽기 권한이 필요하다.

> - [사용 예]
> - cp abc.txt cba txt : cba.txt라는 이름으로 바꿔서 복사
> - cp -r abc cba : 디렉터리 복사

### touch
크기가 0인 새 파일을 생성하거나, 이미 파일이 존재한다면 파일의 최종 수정 시간을 변경한다.

> - [사용 예]
> - touch abc.txt : 파일이 없을 경우엔 abc.txt라는 빈 파일을 생성하고 abc.txt가 있을 경우엔 파일의 최종 수정 시간을 현재 시각으로 변경

### mv
MoVe의 약자로 파일이나 디렉터리의 이름을 변경하거나 다른 디렉터리로 옮길 때 사용한다.

> - [사용 예]
> - mv abc.txt /etc/sysconfig/ : abc.txt을 /etc/sysconfig/ 디렉터리로 이동
> - mv aaa bbb ccc ddd : aaa, bbb ,ccc 파일을 "/ddd" 디렉터리로 이동
> - mv abc.txt www.txt : abc.txt의 이름을 www.txt로 변경해서 이동

### mkdir
MaKe DIRectory의 약자로 새로운 디렉터리를 생성한다. 생성된 디렉터리는 명령어를 실행한 사용자의 소유가 된다.

> - [사용 예]
> - mkdir abc : 현재 디렉터리 아래에 '/abc'라는 디렉터리 생성
> - mkdir -p /def/fgh : /def/fgh 디렉터리를 생성하는데, 만약 'fgh'의 부모 디렉터리인 '/def' 디렉터리가 없다면 자동으로 생성

### rmdir 
ReMove DIRectory의 약자로 디렉터리를 삭제한다. 해당 디렉터리의 삭제 권한이 있어야 하며, 디렉터리는 비어 있어야 한다. 파일이 들어 있는 디렉터리를 삭제하려면 'rm -r'을 실행해야 한다.
> - [사용 예]
> - rmdir abc

### cat
conCATenate의 약자로 파일의 내용을 화면에 보여준다. 여러 개 파일을 나열하면 파일을 연결해서 보여준다.
> - [사용 예]
> - cat a.txt b.txt : a.txt 와 b.txt를 연결해서 파일의 내용을 화면에 보여준다.

### head & tail
텍스트 형식으로 작성된 파일의 앞 10행 또는 마지막 10행만 화면에 출력한다.
> - [사용 예]
> - head -3 anaconda-ks.cfg : 앞 3행만 화면에 출력

### more
텍스트 형식으로 작성된 파일을 페이지 단위로 화면에 출력한다. 스페이스바를 누르면 다음 페이지로 이동하며, b를 누르면 앞 페이지로 이돈한다. q를 누르면 종료한다.

### file
해당 파일이 어떤 종류의 파일인지를 표시해준다.

> - [사용 예]
> - file anaconda-ks.cfg : anaconda-ks.cfg는 텍스트 파일이므로 아스키파일 (ASCII)로 표시된다.
> - file /usr/bin/gzip : gzip은 실행 파일이므로 Executable 파일로 표시된다.

### clear
현재 사용 중인 터미널 화면을 깨끗하게 지워준다.



