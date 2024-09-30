FROM openjdk:11-jre-slim

ENV JMB_VERSION 0.4.3-bypass-fix

#No downloadable example config since 0.2.10
RUN mkdir -p /jmb/config
ADD https://github.com/sks316/MusicBot/releases/download/$JMB_VERSION/JMusicBot-$JMB_VERSION.jar /jmb/JMusicBot.jar

COPY ./docker-entrypoint.sh /jmb
COPY ./config.txt /jmb/config

RUN chmod +x /jmb/docker-entrypoint.sh

ENTRYPOINT ["/jmb/docker-entrypoint.sh"]
