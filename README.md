# recipe-api-api
A recipe API project where users can upload and manage their recipes, add tags, ingredients and images to them.

**Setup**:

+ The application runs on a docker container.

+ There are two docker-compose files in the root directory, the "docker-compose.yml" is used for the application development, the "docker-compose-deploy.yml" is used in production.

+ Fork the repository and clone it to your local computer,

+ Open your cmd and navigate to the project folder,

+ Run the **docker build -t 'image-name' .** command to build the app's image with its Dockerfile (it should automatically install all the requirements in the requirements.txt file.).

+ Once the build is complete, run the **docker-compose up** command to get the application started. The server should start at http://localhost:8000.
  
**Features**: 
+ Each functionalities have comments in them to explain what it is doing.
  
+ A user authentication system that uses django's token authentication. A user is assigned a token on signup or login to use on subsequest requests till it is expired by django.
  
+ The validation methods also checks for short passwords, ensures a password is not less than 5 characters.
+ Users can upload their recipe names, images, tags and ingredients assiociated with it.
+ Recipes are created with a foreign key relationship linking to the user that created it(unauthenticated users can't create recipes).

+ **Nginx** is added for reverse proxying(to handle static files while uWsgi handles the dynamic content).

+ Application functionalities thoroughly tested with unit and integration tests.

+ The software's architecture is pretty good for medium-sized application, would be improved as demands increases.

+ **Tech stacks - Docker, Django rest framework, Nginx, postgresQL.**

Development paused but still open for contributions.

**Contact - +2348168958556 --momsdboy@gmail.com - email**
