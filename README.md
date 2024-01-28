# DevOps-Assignment-2 (Part 2)
DevOps-Assignment-2 (Part 2)

 - Create a Docker file for the web application container which should include the necessary
dependencies to run the web application. The web application should display a simple
"Hello, World!" message when accessed from a web browser
    - In the web/app/index.py file I have created web application in fastapi which will display "Hello, World!"

 - Create a Docker file for the database container which should include the
necessarydependencies to run the database. You can use any database of your
choice (e.g.,MySQL, PostgreSQL, MongoDB, etc.). 
    - In database/Dockerfile it is creating docker image of mysql
    - docker build -t my-mysql-image .
    - docker run -d -p 3306:3306 --name my-mysql-container my-mysql-image    
 - Create a docker-compose.yml file that defines the two services - web and database. The
    web service should be linked to the database service using Docker Compose
    networking.
    - At the root directory there is docker-compose.yml file which is joining 2 services web and database part and we can run it using this command: docker-compose up    
 - Use the docker-compose up command to build and run the application. Verify that the
    web application is accessible from a web browser and that the database is running. 
    - docker-compose up   
 - Modify the Docker file for the web application container to include a new feature (e.g.,
    a new message, a new page, etc.). Rebuild the web application container and
    redeploy the application using docker-compose. Verify that the new feature is working
    as expected.   
    - In web/app/index.py file new feature is added and running docker-compose up again
 - Implement a backup strategy for the database. This can be achieved using a Docker
    volume or by running a backup script periodically  
    - Added volume feature in docker-compose.yml file now it will persist or save last image state even if docker is shutdown of somehow not working
 - Implement a scaling strategy for the web application. This can be achieved by using the
    docker-compose scale command to create multiple instances of the web service. Verify
    that the web application is accessible and working correctly when scaled.
    - docker-compose up -d --scale web=3 (any number)
 - Implement a monitoring strategy for the application. This can be achieved by using a tool
    like Prometheus or Grafana to monitor the health and performance of the containers.
    - Added functionalities now it will provide real-time monitoring, visual dashboards, and alerts for quick issue detection and performance analysis, enhancing overall system reliability and performance.  

 
    