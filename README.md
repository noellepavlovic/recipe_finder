# Project Proposal: Recipe Helper


## Project Goal

- I would like learn how to integrate authentication, authorization into an application
- I would like to learn how to create a CRUD app using a database and integrate this with the authentication and authorization.
- I will use a 3rd party recipe api for recipe queries.  I will make these queries using a server.  I would like to stregthen my ability to do this.
- I would like to create a full stack application.




## Tech Stack

### First Party Tools
- React for building out the UI, along with a UI framework such as Bootstrap or Materialize
- Node and express to communication between Recipe API and server, and the server and the UI.
- nodejs, Passport and postgres for authentication
- postgres for database with Knex and bookshelf for ORM
- token based authorization using JWTs and Postgres



### Third Party Tools
- I will be using one of the following recipe api's:
  
	- Spoonacular API
	- Edamam API
	- Yummly API 

	I am waiting for approval to use these for educational purposes, otherwise there would be a charge.
- Github for source code	


## Features and Deliverables
- The recipe helper application will allow the user to go to the site and enter a number of ingredients that they have at home.  
- The site will return a list of recipes that match the ingredients in their search criteria.
- the user will be able to click on the recipe to bring up a full page which details the recipe.
- the user can choose to leave the site after this, go back to their search or they can create an account and save the recipes to a "recipe box".

### Future deliverables:

- add the functionality for users to have multiple recipe boxes
- for the user to add their own recipes to their recipe boxes 
- have the ability to share their recipes with other users of the system, so that their recipes would also be returned in a search for meal ideas.
- a mobile app version of the recipe helper site


## Data

### User 
The user may or may not have an account to login and store their recipes.  If they require an account they will need to register by providing their name, a valid email address and password. 

The user model:

	id: unique_id
 	firstName: String
 	lastName: String
 	email: String
 	password: Hash
 	recipebox_id: foreign_key
 			

### Ingredients
The ingredient will be inputted by the user through the UI and an api call will be sent to the api using the ingredients as query parameters.  

### Recipes
Recipes will be provided by a 3rd party recipe api (see above).  The data will be extracted from the data sent from the api and then rendered on the UI. If the user would like to save the object, they need to be authenticated and then they can save to their recipe box

The recipe model:

	id: unique_id
 	recipeName: String
 	ingredients: String
 	instructions: String
 	classification: String
 	

