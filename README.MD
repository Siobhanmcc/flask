## Introduction

This is the milestone project that I have created for the “Data Centric Development” module, which is part of “Full Stack Web Development Course” offered by Code Institute.

I love cooking and trying new recipes. I usually collect recipes from Youtube and other public sites and adapt them to my taste. This was a perfect opportunity to build a cookbook application where I can save all my favorite recipes at one source and share with my friends who ask me for recipes. 
It also allows others to add and store their recipes securely. The link for the site is here: http://flask-project-milestone-3.herokuapp.com

![](static/images/scr-shot-across-devices.png)

## User Stories

As a regular user, I want to be able to:

- Register as a new user
- View the recipes from any device (mobile, tablet, desktop).  
- See recipes from other users to get new ideas.  
- View all recipes as a Guest.  
- Search any specific recipe.  
- Login and add my recipes.[Create]  
- Get the instruction to make a dish from this site.[Read]  
- Edit the recipes I've added.[Edit]  
- Delete the recipes I've submitted.[Delete]    

As an admin user, I want to be able to:  

- Manage categories i.e. add new categories, edit existing ones & delete old ones


## Design Framework

[Materialize 1.0.0](https://materializecss.com/)

To get a modern and clean layout, I used Materialize as a framework.

[jQuery 3.4.0](https://jquery.com/)

Used to manipulate the DOM, for example buttons, and showing / hiding elements

[Flask 1.0.2](https://flask.palletsprojects.com/en/2.0.x/)

Flask is the micro web framework that runs the application

## Database
For the database, I chose MongoDB and this was a great opportunity to get experience using NoSQL database MongoDB.

See the database schema here

The database is made up of the following collections

### *categories*
| Property name | Type |
| ---- | ------- |
| id | ObjectId |
| category_name | string |


### *recipes*
| Property name | Type |
| ---- | ------- |
| id | ObjectId |
| category_name | string |
| recipe_name | string | 
| recipe_description | string |
| created_by | string  |

### *users*
| Property name | Type |
| ---- | ------- |
| id | ObjectId |
| username | string |
| password | string |

## Color Scheme
For the color scheme, I've used blue in the navbar. I chose green and red for some buttons and headings to highlight. 

## Typography
The following font was used:

Arial

## Icons
Materialize icons was used for this project.

## Wireframes
Mock-ups were created early on in this project.

![](static/images/login.png)
![](static/images/profile.png)
![](static/images/home.png)
![](static/images/newrecipe.png)
![](static/images/managecategories.png)

## Features
### Existing Features

*For visitors to the site who are not logged in, the following links are available for them to use.*

 a. Home

 b. Login

 c. Register

*For users who are logged in, the list of items is as follows:*

 a. Home

 b. Profile

 c. New Recipe

 d. Logout

*For admin users, the list of items is:*

 a. Home

 b. Profile

 c. New Recipe

 d. Manage Categories

 e. Logout

### Register User

Users can use the site as a guest, but some features are not available unless logged in.I have built-in authentication and authorization to check certain criteria is met before an account is validated. All passwords are hashed for security purposes!

When a user registers,they are automatically logged in and directed to the Profile page.

### Log In to Account

The login page has an input form like register form where the users will enter their username and password.

If the username is not registered or if the password is incorrect an error message will appear.

New users can click on the link "Register here" to get redirected to the register page.

### Log Out of Account

Users can easily log out of their account with the click of a button.

### Home

On the home page, all recipes are displayed.

### Search recipe

If a user would like to search for something specific, there is a search functionality on the home page.

### New Recipe

[CRUD] Create or 'add' a new recipe.

Logged in users can add their recipes.

### View Recipe

[CRUD] Read or 'review' recipes, from the home page.

### Update Recipe

[CRUD] Update or 'edit' their own user recipes from the home page.

### Delete Recipe

[CRUD] Delete or 'remove' a user's own recipes.

If the user clicks the Done button, the user can delete a recipe.

### Manage Categories 

A user with admin access can login and add, edit or delete a category. 

## Technologies Used

Languages

- HTML used as the markup language

- CSS used as the base for cascading styles.

- JavaScript used mostly for DOM manipulation

- Python3 used to run the backend application

Libraries

- Google Fonts provided the fonts used throughout the project

- Font Awesome v5.8.2 to provide the icon set

- Materialize v1.0.0 used as the CSS framework for the project

- jQuery used as the primary JavaScript functionality.

- Flask v1.0.2 is the micro web framework that runs the application

- Jinja v2.10.1 is the default templating language for flask and is used to display data from the python application in the frontend html pages

- PyMongo 2.3.0 was used to enable the python application to access the Mongo database

Tools

- MongoDB Atlas is used to store my database in the 'cloud'.

- Git is used for version control

- GitHub provides hosting for software development version control using Git

- Balsamiq was used to create the wireframes when initially planning this project

## Hosting
Heroku is used to host the app

## Testing
Creating an Account

1. I've created my own account, and other accounts to confirm authentication and validation for creatiing account and all worked as expected.
![](static/images/login3.png)
On registering an account, the user receives a message saying "Registration successful".
![](static/images/register-success.png)

2. Log In To An Admin Account

A user can login into an Admin account to see the full functionality of the menu. 

![](static/images/Admin.png)

Upon logging in, there are 5 options on the navbar including 'manage categories' which is exclusive to the admin view. The user is directed to the Profile page.

![](static/images/admin-profile.png)

3. Log Out

Upon logging out of the application, a user receives a notification saying "You have been logged out".
![](static/images/logged-out.png)

4. New Recipe 

I have successfully added new recipes.

![](static/images/beef-stew.png)

These recipes are then visible on the home page and can be edited or deleted from there.

![](static/images/beef-stew-added.png)

![](static/images/edit-recipe2.png)

5. Search functionality

I have searched for recipes using the search functionality on the home page. Results come back correctly.

![](static/images/cookies.png)
![](static/images/cookie-results.png)

6. Manage Categories

I have successfully added categories. 
![](static/images/manage-categories.png)
![](static/images/add-category.png)

If you wish to test the site yourself you can do this with:

Username: siobhan Password: testpassword

or Admin User

Username : Admin Password: ungoo4La

## Validation Services

The following validation services were used to check the validity of the website code.

W3C Markup Validation was used to validate HTML.

W3C CSS validation was used to validate CSS.

JSHint was used to validate JavaScript.

PEP8 Online was used to validate the app.py file. 

Responsiveness  

Chrome DevTools and physical devices were used throughout development for a number of purposes, one of which was to test the responsiveness and rendering across a range of sizes and devices. As issues were found they were either fixed at the time or noted and returned to later.

The site has been tested successfully on

Apple Macbook Air - Safari browser
Apple iPhone 6,7 &8S - Safari Browser
iPad Mini - Safari Browser
Desktop - Chrome v.74
Desktop - Firefox v.67

## Deployment
### Deployment To Heroku
In order the deploy my project to Heroku I have completed the following steps:

1. Created a Procfile with the command echo web: python run.py > Procfile.
2. Created a requirement.txt file so Heroku know what python modules it will need to run my    application with the command sudo pip freeze --local > requirements.txt
3. Then git add and git commit the new prerequisites from the requirements.txt file and Procfile, then 'git push' the undertaking to GitHub.
4. Created config Vars such as my Secret Key, IP PORT and MONGO_URI within .bashrc so I could still run the project from my own IDE

### Heroku

After logging into Heroku:

1. I created a new app, using the name flask-project-milestone-3 and set the region to Europe.

2. In the settings tab I clicked reveal config vars and entered the required environment variables, which in this case were:

- IP 0.0.0.0

- PORT 5000

- MONGO_URI mongodb+srv://root:r00tUser@myfirstcluster.qi6w0.mongodb.net/task_manager?retryWrites=true&w=majority

- SECRET secret key for flask session

3. From the Heroku dashboard of the newly created application, I clicked on "Deploy" > "Deployment method" and select GitHub.

4. I confirmed the linking of the Heroku app to the correct GitHub repository.

5. In the Heroku dashboard, I clicked on "Deploy".

6. In the "Manual Deployment" section of this page, I made sure the master branch is selected and then click "Deploy Branch".

The site was now successfully deployed.

### Local Deployment

Should you wish the run a local copy of this application of your local machine, you will need to follow the instructions listed below:

Tools you may need:

[Python 3](https://www.python.org/downloads/) installed on your machine 

[PIP](https://pip.pypa.io/en/stable/installing/) installed on your machine 

[Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03) installed on your machine 

A text editor such as [Visual Studio Code](https://code.visualstudio.com/)

An account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) running locally on your machine

To deploy locally on your own machine, follow these steps:

1. Save a copy of the repo on your local machine or use git clone and cd into the correct folder using the terminal.

2. Create a virtual environment, using python -m venv venv where the 2nd venv is the environment name.

3. Activate the virtual environment with venv\Scripts\activate

4. Install any required modules with pip install -r requirements.txt

5. Within the file app.py change the line app.config['SECRET_KEY'] = os.getenv('SECRET') to app.config['SECRET_KEY'] = os.getenv('SECRET', '<your_key>) where <your_key> is a secret key of your choosing.

6. Also change app.config["MONGO_URI"] = os.getenv('MONGO_URI') to app.config["MONGO_URI"] = os.getenv('MONGO_URI', ) where is the string that points to your own MongoDB.

7. From the terminal you can then run the app with python app.py and view in a browser at http://127.0.0.1:5000/

## Credits

Content
The recipes for the cookbook were sourced from various sources.

The text for some of the recipe categories was taken from Wikipedia.

The mini-project on backend development from Code Institute provided a basis for this app. 

## Acknowledgements
Tutorials

[Tutorials Point](https://www.tutorialspoint.com)

[Stack Overflow](https://stackoverflow.com)

[YouTube](https://www.youtube.com/watch?v=vVx1737auSE) - To understand how to create the login/register functions.

[Quackit](https://www.quackit.com/mongodb/tutorial/mongodb_sort_query_results.cfm)

Special thanks to Guido Cecilio Garcia, my Code Institute mentor, for his guidance and advice whilst working on this project.




