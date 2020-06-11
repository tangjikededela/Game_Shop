# README for the Application

The application is an online game store allowing registered users to order games. In addition, it visualize the sales data in a heat map.

The development environment use SQLite and production environment use PostgreSQL as the database management system.

Ruilin Wang   51986323

## Demo of the Application
A live version is deployed on Heroku, and can be accessed using the following link:

https://shrouded-fjord-26206.herokuapp.com/
 
## Data Sources
The data of games are from "Video Game Sales with Ratings" dataset on Kaggle
More dteails informations are in https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings
The data only include the games on ps, ps4, 3ds platform. 

## System Requirement
The application is built on Ruby on Rails framework, with Bootstrap, JQuery,  Highchart, and Highmap.

### Ruby Version and Gems
Ruby ~> 2.5.1, Rails ~> 5.2.3

filterrific gem is for sorting and filtering function

will-pagination gem is for pagination

More details in the Gemfile

### Bootstrap, JQuery, and JQuery UI
Bootstrap 4.3.1 is loaded from BootstrapCDN.

### Highchart and Highmap
The latest version of Highchart and Highmap are loaded from CDN for data visualization.


## User Authentication

### Default Users
| Email                 | Password           | Admin        |

|:-------------    -:   | ------------- :    | ------------:|

| admin@admin.admin     |   123456           |   True       |

| user@user.user        |   123456           |   False      |


These users are in the Heroku demo, you can use them to test the features of the application.

Only logged in users can place an order and visit all their orders.

Only admin users can manage the databases.

#### Register new user

Visitors can register for a new account.


## Local Deployment of the Application

### Prepare Files
Run ``git clone`` to clone the application from an online repository or download the compressed file and extract it to a local folder.

### Install Dependencies
Execute ``bundle install`` to install all the required gems.

### Initialize Databases

Execute ``rails db:migrate``

### Populate the tables
Execute ``rake games:seed_games`` to populate the ``games and countries`` table.

### Initialize User System
To create default users, execute ``rake db:seed ``.

### Run the Application Locally
When everything is ready, execute `rails server`, then open ``localhost:3000`` in the browser to access the application. You can specify the port by `rails server -p [port_number]`.

### Test 
Unit test:
execute `rails test`

### Features

#### Order games
Logged in users can visit the page showing the details of game and place an order.

#### general text search & filters
In the "Search Games" view, there is a general text search and many different filters.

#### Visualize Data on the World Map
Sales data group by developers' country and time on world map

#### Sorting in the tables
Most the tables in the application including "games" and "orders" can be sorted incrementally or decrementally by clicking the headers.
