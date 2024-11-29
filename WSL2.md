# WSL2

- 명령 프롬프트를 관리자 권한으로 열어 다음 명령어 입력
~~~
C:\> wsl.exe --install
~~~


- 필수 윈도우 기능 활성화
  
![image](https://github.com/user-attachments/assets/6e9f1d77-60e1-4a5c-9a14-817493581bcb)    ![image](https://github.com/user-attachments/assets/03a0ac66-dc5f-4c8b-85fe-a36649a164c8)

~~~
C:\> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
C:\> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
~~~


- WSL을 사용하여 Windows에 Linux를 설치하는 방법
  
  https://learn.microsoft.com/ko-kr/windows/wsl/install#install-yrour-linux-distribution-of-choice

- 설치하는 리눅스 배포판의 WSL2 버전을 기본값으로 설정
~~~
wsl --set-default-version 2
~~~

- Rancher Desktop 설치
  https://rancherdesktop.io

  - Rancher 저장소 서명 추가
  ~~~
  $ curl -s https://download.opensuse.org/repositories/isv:/Rancher:/stable/deb/Release.key | gpg --dearmor | sudo dd status=none of=/usr/share/keyrings/isv-rancher-stable-archive-keyring.gpg
  ~~~

  - Rancher 저장소 추가
  ~~~
  $ echo 'deb [signed-by=/usr/share/keyrings/isv-rancher-stable-archive-keyring.gpg] https://download.opensuse.org/repositories/isv:/Rancher:/stable/deb/ ./' | sudo dd status=none of=/etc/apt/sources.list.d/isv-rancher-stable.list
  $ sudo apt update
  ~~~

  - Rancher Desktop 패키지 설치
  ~~~
  $ sudo apt install rancher-desktop
  ~~~

  - Rancher Desktop 삭제
  ~~~
  $ sudo apt remove --autoremove rancher-desktop
  $ sudo rm /etc/apt/sources.list.d/isv-rancher-stable.list
  $ sudo rm /usr/share/keyrings/isv-rancher-stable-archive-keyring.gpg
  $ sudo apt update
  ~~~
  

- WSL 명령어
  - 배포판 나열
  ~~~
  C:\> wsl --list            # 리눅스 배포판들의 목록
  C:\> wsl --list --running  # 실행 중인 리눅스 배포판들의 목록
  ~~~

  - list 목록에 있는 프로그램 삭제
  ~~~
  C:\> wsl --unregister 대상 프로그램
  ~~~
