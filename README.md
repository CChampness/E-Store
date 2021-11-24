# E-Store
E-Commerce backend using Sequelize

## Overview
The E-Store app is a backend which provides an api to give internet access to a client who wishes to use the RESTful "CRUD" features to access and maintain a database of products, categories, and tags for an e-commerce store.  The app uses the Sequelize library to give an Object-Relational Mapping interface to the database.  The database is relational and it uses three kinds of mappings:
* belongsTo
* hasMany
* belongsToMany

The relationship of the Categories to the Products is one-to-many.

There is also a cross-reference table to support the many-to-many relationship between Products and Tags.

This app uses **Express.js, Sequelize, and MySQL**.


```
This app could be particularly helpful to a manager at an internet retail company who needs a back end for an e-commerce website.  This will enable a company to be more competitive with other e-commerce companies.
```

The following packages are used in this app:
* [MySQL2](https://www.npmjs.com/package/mysql2)
* [Sequelize](https://www.npmjs.com/package/sequelize)
* [dotenv](https://www.npmjs.com/package/dotenv)

## Features
```
* The database name, MySQL username, and MySQL password are stored in an environment variable file for security.
* Initially, the user will enter schema and seed commands: "npm run seed", "node server"
* When the server is started, it syncs the Sequelize models to the MySQL database
* The client API uses GET routes in Insomnia Core for categories, products, and tags
* The data for each of the routes is displayed in formatted JSON
* The client uses the API POST, PUT, and DELETE routes in Insomnia Core to create, update, and delete data in the database
```

## Walkthrough Video of the database using Insomnia:  [Walkthrough video](https://watch.screencastify.com/v/tndAmP87tfIarw9kq4mU)


## Database tables
The database contains the following four tables:

* `Category`
  * `id`
  * `category_name`

* `Product`
  * `id`
  * `product_name`
  * `price`
  * `stock`
  * `category_id`

* `Tag`
  * `id`
  * `tag_name`

* `ProductTag`
  * `id`
  * `product_id`
  * `tag_id`


