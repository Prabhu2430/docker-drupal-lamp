# docker-drupal-lamp
Minimal Drupal 7.x development environment stack. <br/>

How to use:<br/>
1. Place a copy of this docker-compose.yml file at your Drupal site root or maybe create a folder "docker/".<br/>

2. Build the image using 'docker build -t your_image_name .'<br/>

3. Start the web stack: 'docker-compose up -d'<br/>

4. To see your running containers: 'docker ps'<br/>

5. To get inside the container using bash: 'docker-compose exec web bash'<br/>

6. For new installation:
Add Database setup instructions while installing Drupal:
- Database name = 'your_db_name'<br/>
- Database username = 'root'<br/>
- Leave database password blank<br/>
- Expand "Advanced options" and set Database host = 'db' (This is defined in docker-compose.yml file)<br/>

7. For existing installation:
Import Database using:<br/>
docker exec -i your_db_container mysql -uroot -proot your_db_name < filename.sql

8. Make necessary changes in settings.php

