FROM openjdk:8-jdk-alpine

RUN apk add --no-cache bash && \
    apk add --no-cache -t build-dependencies wget && \
    cd /usr/lib && \
    wget https://github.com/JetBrains/kotlin/releases/download/v1.2.0/kotlin-compiler-1.2.0.zip && \
    unzip kotlin-compiler-*.zip && \
    rm kotlin-compiler-*.zip && \
    rm kotlinc/bin/*.bat && \
    apk del --no-cache build-dependencies

ENV PATH $PATH:/usr/lib/kotlinc/bin

CMD ["kotlinc"]
