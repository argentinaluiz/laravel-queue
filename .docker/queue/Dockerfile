FROM argentinaluiz/laravel-queue

USER root

RUN apk --update add supervisor

COPY supervisord.conf /etc/supervisord.conf
COPY supervisord.d/ /etc/supervisord.d

ENTRYPOINT ["/usr/bin/supervisord", "-n", "-c",  "/etc/supervisord.conf"]

WORKDIR /etc/supervisor/conf.d/
