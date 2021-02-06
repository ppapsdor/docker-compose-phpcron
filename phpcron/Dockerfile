FROM ubuntu:20.04
MAINTAINER Patrick Papsdorf

# Timezone
ENV TZ Europe/Berlin

RUN ln -snf /usr/share/zoneinfo/${TZ} /etc/localtime && echo ${TZ} > /etc/timezone

WORKDIR /var/www

RUN apt-get update && apt-get install -y php cron

RUN touch /var/log/schedule.log
RUN chmod 0777 /var/log/schedule.log

ADD scheduler /etc/cron.d/scheduler
RUN crontab /etc/cron.d/scheduler

RUN apt-get autoclean -y && apt-get clean -y

CMD ["cron", "-f"]
