# Food Recipe API
API for managing food recipes using docker and django.

### Setup
Make sure docker is installed and running\
  https://www.docker.com/

To run server type in terminal of the project directory:\
  `docker-compose up`

To run tests and linting type in terminal of the project directory:\
  `docker-compose run app sh -c "python manage.py test && flake8"`

### Basic endpoints for the recipe API

  #### Login
  Go to http://127.0.0.1:8000/api/user/token/ \
  when valid credentials are provided the token is included in the payload.\
  Make sure to include the token in following requests.\
  ![Preview](https://i.imgur.com/MJJKivG.png)

  #### Updating User Information 
  http://127.0.0.1:8000/api/user/me/

  #### Create User
  http://127.0.0.1:8000/api/user/create/

  #### Root Recipe
  http://127.0.0.1:8000/api/recipe/ \
  Includes endpoint URL of components that makes up a recipe (tags, ingredients, etc.).
  
  ### Create Tags
  http://127.0.0.1:8000/api/recipe/tags/
  
  ### Create Ingredients
  http://127.0.0.1:8000/api/recipe/ingredients/
  
  ### Create Recipe
  http://127.0.0.1:8000/api/recipe/recipes/ \
  Recipe created will be added to the user recipe list.
  ![Preview](https://i.imgur.com/5KCBMyn.png)

  #### Recipe Detail
  http://127.0.0.1:8000/api/recipe/recipes/1 \
  Last digit of the URL is the recipe id.
 
  #### Upload Recipe Image
  http://127.0.0.1:8000/api/recipe/recipes/1/upload-image \
  ![Preview](https://i.imgur.com/PAASl1T.png)
  Once the image is uploaded the link to the image is available in the response.\
  ![Preview](https://i.imgur.com/abFDrD0.png)
  

