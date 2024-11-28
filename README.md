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



