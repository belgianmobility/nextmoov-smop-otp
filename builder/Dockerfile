
FROM node:12-buster-slim

RUN mkdir -p /usr/share/man/man1 && apt-get update && \
apt-get install -y default-jdk wget && \
apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /app
RUN wget https://repo1.maven.org/maven2/org/opentripplanner/otp/1.4.0/otp-1.4.0-shaded.jar

COPY ./ /app


VOLUME /data

WORKDIR /app

CMD ["./build"]
