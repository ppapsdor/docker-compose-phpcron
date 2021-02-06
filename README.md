# docker-compose-phpcron
Running a PHP-Script with a cronjob inside a Docker container

Start:
$ docker-compose build
$ docker-compose up -d

The scheduler is started every 10min. This means that the cron.php is started every 10min.

$  docker exec -it docker-compose-cron_phpcron_1 cat /var/log/schedule.log

Example Output:
Datum / Uhrzeit: 06.02.2021 21:50\n
Datum / Uhrzeit: 06.02.2021 22:00\n
Datum / Uhrzeit: 06.02.2021 22:10
Datum / Uhrzeit: 06.02.2021 22:20
Datum / Uhrzeit: 06.02.2021 22:30
Datum / Uhrzeit: 06.02.2021 22:40
