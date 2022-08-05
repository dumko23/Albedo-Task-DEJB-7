# Albedo-Test-Task №7
ALbedo Internship Task


### How to run this project?
##### ```Docker``` and ```Docker Compose``` are required to run this project!


```sample.env.example``` is located in project root folder. Create your own ```.env``` file to adjust project configurations.


1. While in your root folder, use ```git clone``` to get your Laravel project
2. Adjust following section to configure Laravel you want to run using cloned project name:
```
APP_PATH_HOST=./Albedo-task-DEJB-3
```
3. If you running project with Docker - in project root terminal write ```docker-compose build``` and ```docker-compose up -d``` to create and run project docker container in detached mode.
4. From your root folder's terminal, run ```docker-compose run --rm npm install``` to install npm packages.
5. Open your php container's terminal, run ```composer install``` to install dependencies.
6. In your root folder's terminal, run ```docker-compose run --rm npm run watch``` to run webpack mix watch command.
7. In your php container's terminal, run:
```
sudo chmod -R 777 storage
php artisan cache:clear
php artisan config:clear
php artisan config:cache
``` 
This will fix permission problems with your project.
7. Your project is ready. You now can visit your project at ```localhost:8000```
