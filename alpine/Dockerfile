FROM alpine

RUN apk add --no-cache openssh \
    && sed -i s/#PasswordAuthentication.*/PasswordAuthentication\ no/ /etc/ssh/sshd_config \
    && rm -rf /var/cache/apk/* /tmp/* 

COPY entrypoint.sh /usr/local/bin

ENTRYPOINT ["entrypoint.sh"]

