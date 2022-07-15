# docker_workflow_php_apache_mongo
Docker workflow

Created as example for sbd.local project

1. The mongo folder is a separate project, and it runs separately from its own folder.
2. sbd.local is the folder of your local project. When you start the docker-compose, the php and apache images are state separately and join in docker-compose file.
3. Project repository code need to locate in src folder.
4. Create or edit configs files (config.ini or local.ini or other) as your need.
5. To connect your local project to mongo db you need to put the following in your config file:
    - host = "mongo"
    - username	= ""
    - password	= ""
6. In "mongo/docker-assets/mongo/data" you can put databases for further importing from inside "mongo docker container".
