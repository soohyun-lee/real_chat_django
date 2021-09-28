FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY . .
RUN mkdir /logs

RUN apt-get install -y python3-pip python3-dev

# upgrade pip
RUN pip install --upgrade pip


### 실행 환경 구축 ###
# 컨테이너 내부에 config(설정파일)가 들어갈 폴더 생성
RUN mkdir /config

# 호스트에 있는 requirements.txt 파일을 컨테이너 내부로 복사해준다.
ADD /config/requirements.txt /config/

# requirements.txt에 있는 파이썬 패키지 설치
RUN pip install -r /config/requirements.txt

### 작업 디렉토리 ###
# Django 소스코드가 들어갈 폴더 생성
RUN mkdir /src;

# 작업 디렉토리 src로 변경
WORKDIR /src