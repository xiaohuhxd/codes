FROM 8.142.126.97:5000/library/python:3.7
MAINTAINER hushuai <email=1758224505@qq.com>
RUN mkdir /micro -p
ADD run-docker.sh /micro/run.sh
ADD ftp_log.sh	/micro/ftp_log.sh
RUN cd /micro&&chmod u+x *
ADD target/*-exec.jar /micro
EXPOSE 8079
ENV PATH=${PATH}:/micro
ENV S_ACTIVE=${S_ACTIVE:-dev}
ENV JAVA_OPS=${JAVA_OPS:-'-Xms128M -Xmx128M'}
ENTRYPOINT ["run.sh","console"]