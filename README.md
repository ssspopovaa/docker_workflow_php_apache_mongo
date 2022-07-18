# docker_workflow_php_apache_mongo
Docker workflow

Created as example for sbd.local project

1. The mongo folder is a separate project, and it runs separately from its own folder (this container is started first).
   -- all servers use 4.0 mongodb version.
2. php7_1, php7_4 and php8_1 is the folders of your local projects (need to select the required version, depending on the PHP version of the project). When you start the docker-compose, php and apache images are state separately and join in docker-compose file.
3. Project repository code need to locate in src folder (git clone...).
4. Create or edit configs files (config.ini or local.ini or other) as your need.
5. To connect your local project to mongo db container you need to put the following in your config file:
    - host = "mongo"
    - username	= ""
    - password	= ""
6. In "mongo/docker-assets/mongo/data" folder you can put databases for further importing from inside "mongo docker container".
