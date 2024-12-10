Git Bash에서 container-shell로 접근하려면 winpty docker 사용해야하는데
docker 명령어를 변경해서 사용한다

~~~
echo "alias docker='winpty docker'" >> ~/.bashrc
~~~

Git Bash에서 "alias" 명령어를 실행 했을 때 아래 처럼 나오면 정상

<img width="443" alt="image" src="https://github.com/user-attachments/assets/7ff75754-9600-46d1-9cda-f5392cb9c24d">
