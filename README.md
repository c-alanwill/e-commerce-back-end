# E-Commerce Back End

## Description

The application shows the back end for an e-commerce site.  Categories, products and product tags can be viewed, created, updated and deleted in the app.  The command-line application uses Express.js API and Sequelize to interact with a MySQL database. 


## Functionality

Give a functional Express.js API, when a user adds a database name, a MySQL user name and a MySQL password to an enviroment varialbe file, then the user can connect to the database using Sequelize.

When schema and see commands are entered, a development database is created and is seeded with test data.

When the command-line application is invoked by using typing npm start in the terminal, the server is started and the Sequelize models are synced to the MySQL database.

When the user opens API GET routes in Insomina for categories, products or tags, then the data for each of these routes is displayed in formatted JSON.  When the user tests API POST, PUT, and DELETE routes in Insomnia, they are able to successfully create, update and delete data in the database.


## Database Models

The database contains the following four models, including the requirements listed for each model: 
 **Category** 
* id;
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
* category_name
    * String.
    * Doesn't allow null values.

 **Product** 
* id;
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
* product_name;
    * String.
    * Doesn't allow null values.
* price;
    * Decimal.
    * Doesn't allow null values.
    * Validates that the value is a decimal.
* stock;
    * Integer.
    * Doesn't allow null values.
    * Set a default value of '10'.
    * Validates that the value is numeric.
* category_id
    * Integer.
    * References the 'Category' model's 'id'.

 **Tag** 
* id;
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
* tag_name
    * String.

 **ProductTag** 
* id;
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
* product_id;
    * Integer.
    * References the 'Product' model's 'id'.
* tag_id;
    * Integer.
    * References the 'Product' model's 'id'.

## Code

The application uses [MySQL2](https://www.npmjs.com/package/mysql2) and [Sequelize](https://www.npmjs.com/package/sequelize) packages to connect the Express.js API to a MySQL database and the [dotenv](https://www.npmjs.com/package/dotenv) package to use environment variables to store sensitive data.

Comments have been applied to the different files in the code to identify each section of code. 

There is a server.js file that starts the application.

Included is a package.json file with the required dependencies, as well as gitignore, node_modules and .DS_Store files.


## Installation

The code for this project can be found on GitHub at: https://github.com/c-alanwill/e-commerce-back-end

A link to a video that shows a walkthrough demonstrating how this readme works is available at: https://drive.google.com/file/d/1LbMaf-oCZAyz0RuBnghwuU8FAc5D0NhD/view


## Usage

The following animation shows the application's GET routes to return all categories, all products, and all tags being tested in Insomnia:

![In Insomnia, the user tests “GET tags,” “GET Categories,” and “GET All Products.”.](./Assets/13-orm-homework-demo-01.gif)

The following animation shows the application's GET routes to return a single category, a single product, and a single tag being tested in Insomnia:

![In Insomnia, the user tests “GET tag by id,” “GET Category by ID,” and “GET One Product.”](./Assets/13-orm-homework-demo-02.gif)

The following animation shows the application's POST, PUT, and DELETE routes for categories being tested in Insomnia:

![In Insomnia, the user tests “DELETE Category by ID,” “CREATE Category,” and “UPDATE Category.”](./Assets/13-orm-homework-demo-03.gif)


## Credits

N/A

## License

Please refer to the license in the repo.

## Contributing

N/A