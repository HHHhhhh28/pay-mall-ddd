# 基础镜像
FROM openjdk:8-jdk-alpine

# 作者
MAINTAINER zky

# 配置
ENV PARAMS=""

# 时区
ENV TZ=PRC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# 添加应用
ADD target/s-pay-mall-ddd-zky-app.jar /s-pay-mall-ddd-zky-app.jar

ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /s-pay-mall-ddd-zky-app.jar $PARAMS"]