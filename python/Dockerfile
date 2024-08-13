FROM bitnami/python:3.12-debian-12

# install Curl for HealthCheck
#RUN apt update -y && apt install -y curl

WORKDIR /app

#ENV PYTHONDONTWRITEBYTECODE=1
#ENV PYTHONUNBUFFERED=1

# change Container TimeZone To Tehran
#ENV TZ="Asia/Tehran"
#RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY ./requirements.txt requirements.txt

RUN pip install -i https://mirrors.aliyun.com/pypi/simple/ --upgrade pip
RUN pip install -i https://mirrors.aliyun.com/pypi/simple/ -r requirements.txt

COPY . /app

CMD ["python", "consumer.py"]
