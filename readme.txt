# Create mysql container to be used for multiple work projects

	sudo docker-compose up -d

# For importing databases manually:

    * Attach to mysql container
        sudo docker exec -it mysql bash
        mysql -uroot -psecret
   
    * Run these commands in mysql
        set global max_allowed_packet=268435456;
        GRANT ALL PRIVILEGES ON *.* TO 'homestead'@'%';

    * Copy sql files to root project directory for access by Docker
        sudo docker exec -i mysql mysql -uroot -psecret dbName < fileName.sql 

# Mysql container port
	
     mysql - :3306

# Mysql credentials

    host: mysql
    user: root
    pass: secret
