FROM python:2.7-stretch

LABEL Saliou DIABATE diabate.ci@gmail.com

RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y \
&& pip install flask flask_httpauth flask_simpleldap python-dotenv

RUN mkdir /data

ADD ./student_age.py /student_age.py
ADD ./student_age.json /data/student_age.json

EXPOSE 5000

VOLUME /data

WORKDIR /

CMD [ "python", "./student_age.py" ]