# home_work_2
1: Задание![1:Задание](work_home_2/1%20задание/1.1.png)


2: Задание


![скриншот](work_home_2/2%20задание/2.1.png)


3: Задание
![Описание изображения](work_home_2/3%20задание/3.1.png)

4: Задание


![Описание изображения](work_home_2/4%20задание/4.1.png)

4: Задание
https://github.com/Skryko/shvirtd-example-python



5: Задание
![Описание изображения](work_home_2/5%20задание/5.1.png)


5: Задание


#!/bin/bash
set -e

ENV_FILE="/opt/app/.env"

if [ -f "$ENV_FILE" ]; then
    export $(grep -v '^#' "$ENV_FILE" | xargs)
else
    echo "Файл $ENV_FILE не найден!"
    exit 1
fi

BACKUP_DIR="/opt/backup"
mkdir -p "$BACKUP_DIR"

NOW=$(date +"%Y-%m-%d_%H%M%S")
BACKUP_FILE="${BACKUP_DIR}/backup-${NOW}.sql.gz"

docker exec -i app-db-1 mysqldump -u"$MYSQL_USER" -p"$MYSQL_PASSWORD" "$MYSQL_DATABASE" | gzip > "$BACKUP_FILE"

ls -lh "$BACKUP_FILE"



5: Задание


* * * * * /opt/backup/backup.sh >> /opt/backup/backup.log 2>&1



6: Задание


![Описание изображения](work_home_2/6%20задание/6.1.png)


6: Задание


![Описание изображения](work_home_2/6%20задание/6.2.png)



6.1: Задание


![Описание изображения](work_home_2/6.1/6.1.1.png)

6.2: Задание



![Описание изображения](work_home_2/6.2/6.2.1.png)










