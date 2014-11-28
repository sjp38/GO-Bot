# 환경설정 

텔레그램과 GO 언어 환경 설정을 위해 컨테이너 환경 [Docker](https://www.docker.com/)를 사용합니다. 컨테이너 환경은 경량 가상 머신으로 생각하셔도 무방합니다.

## 코드랩 리포지토리 다운로드

git에 친숙하면 아래와 같이 커맨드 라인에 입력해주세요.

````
git clone https://github.com/GDG-Korea/GO-Bot.git
cd GO-Bot
````

친숙하지 않다면 [ZIP 다운로드](https://github.com/GDG-Korea/GO-Bot/archive/0-setup.zip)를 이용하셔도 됩니다.

## 우분투 환경

````
sudo apt-get update
sudo apt-get install docker.io
````

## Boot2Docker 설정 (맥, 윈도우즈 사용자만)

윈도우즈 환경과 맥 환경은 [Boot2Docker](https://github.com/boot2docker/boot2docker)를 이용하여야 합니다. Docker가 리눅스 환경 위에서만 동작하는 경량 환경이기 때문에 Boot2Docker는 리눅스 가상 머신 위에 Docker 환경을 설정해줍니다. [윈도우](https://docs.docker.com/installation/windows/)와 [맥](https://docs.docker.com/installation/mac/) 사용자는 링크를 읽고 Boot2Docker를 설치하십시오.

### 초기화

````
boot2docker init
````

### 작동

````
boot2docker up
$(boot2docker shellinit)
````

## Docker 이미지 빌드

Docker 이미지 빌드에 관심이 있는 분은 [여기](https://github.com/GDG-Korea/GO-Bot/tree/0-setup/docker)를 참고해주세요.

## Docker 이미지 내려 받기

````
docker pull dalinaum/gobot
````

네트워크 상황 때문에 받기 어려운 경우도 있습니다. 그럴 경우에는 tar 파일을 이용해주십시요.

````
docker load --input gobot.tar
````

## Docker 이미지 수행하기

````
docker run -it dalinaum/gobot
````

만약 직접 이미지를 빌드한 경우에는 `dalinaum/gobot`이 아닌 `gobot`등으로 수행해야 합니다. 빌드 때 사용했던 `-t` 옵션을 참고해주세요.
