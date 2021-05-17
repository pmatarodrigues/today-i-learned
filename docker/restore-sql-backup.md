# Restore SQL backup to container

Get container id
$ `docker ps`

Copy .sql file into container
$ `docker cp BACKUP.sql [container_id]:/BACKUP.sql`

Login into container
$ `docker exec -it [container_id] /bin/bash`

Login into mysql (the next steps can be adapted depending on which database service we are using)
$ `mysql -u USER -p`

Select database
> `use DATABASE-NAME`

Import backup file
> `source BACKUP.sql`