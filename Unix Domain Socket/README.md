# ■ Unix Domain Socket

Unix Domain Socket은 IPC socket (Inter-Process Communication Socket) 이라고도 불리며, TCP (전송 제어 프로토콜, Transmission Control Protocol)의 소켓과 동일한 구조로 데이타를 주고 받을 수 있는 `Local File` 형식 기반의 소켓입니다. 즉, `동일한 시스템 내에서 파일을 통하여 실행되는 프로세스들 사이의 양방향 데이터 교환을 허용하는 프로세스 간 통신 메커니즘`이다.

* Unix Domain Socket은 `localhost`의 각 Process 통신이 되므로 속도가 매우 빠르며 메모리 사용량이 적다는 장점이 있습니다.

* TCP (전송 제어 프로토콜, Transmission Control Protocol) 프로토콜을 사용하는 네트워크 작업과 달리 UDS (Unix Domain Socke)는 Routing 작업을 수행하지 않습니다.

* UDS (Unix Domain Socke) 사용하여 통신 작업을 수행할 경우에는 `Local File` 파일 단위로 통신 작업이 이루어지기에 파일에 접근권한을 제어하여 간단하게 서버와 클라이언트 단위로 프로세스 통신을 제어할 수 있습니다.

## 🛠 Unix Domain Socket 관련 명령어

* `L` → [lsof](https://terms.naver.com/entry.naver?docId=4125712&cid=59321&categoryId=59321): 실행 중인 파일과 프로세스의 정보를 출력하는 명령어입니다. 시스템 전체의 UDS (Unix Domain Socket) 목록을 확인하기 위해서는 `-U` 옵션을 사용합니다.

* `L` -> [ls](https://terms.naver.com/entry.naver?docId=4125708&cid=59321&categoryId=59321): 디렉터리 목록을 출력하는 명령어입니다. 디렉터리 내부의 파일들에 대한 UDS (Unix Domain Socket) 사용여부를 확인하고자 하는 경우에는 `-luh` 옵션을 사용합니다. 디렉터리나 파일의 권한을 나타내는 부분에 `s` 문자가 표시 된 파일은 UDS (Unix Domain Socket) 통신을 수행하고 있는 소켓 파일을 나타냅니다.

`sdrwxr-xr-x   5 mari  staff   160B  9 30 21:21 Developer`

## 📣 REFERENCE

* `WEB` → [유닉스 리눅스 명령어 사전](https://terms.naver.com/list.naver?cid=59321&categoryId=59321)
