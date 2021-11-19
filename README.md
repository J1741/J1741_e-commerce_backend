# J1741 E-Commerce Backend

## Description

E-Commerce Backend is an application that uses an ORM to connect an Express server to a MySQL database, and allows users to perform various CRUD operations via API routes defined in the application.

Technologies used by the application include the `dotenv`, `express`, `mysql2`, and`sequelize` npm packages, as well as the `Node.js` JavaScript runtime and a local `MySQL` database. Detailed installation requirements, steps, and usage instructions are provided below.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Application Demo](#application-demo)
- [Questions](#questions)

## Installation

### Requirements

Before installing the application, be sure you have installed `Node.js` JavaScript runtime, the `npm` package manager, and are running a local `MySQL` server. For more information on these prerequisite technologies, see:

- `Node.js`: https://nodejs.org
- `npm`: https://www.npmjs.com,
- `MySQL`: https://www.mysql.com

Additionally, to test and use the application, make sure you have installed or are logged into an API testing platform like [Insomnia](https://insomnia.rest/)

### Steps

Step 1. Clone the project repo here: https://github.com/J1741/J1741_e-commerce_backend

Step 2. Run the following command in the root of the project directory to install the application:

```
npm i
```

This will install the necessary dependencies for the application to run.

Step 3. Rename the `.env.EXAMPLE` file to `.env`. This will ensure the credentials we enter in Step 4 are not pushed up to GitHub.

Step 4. In the newly renamed `.env` file: replace the string USERNAME with your local MySQL username, replace the string PASSWORD with your local MySQL password, and save these changes to the file.

Step 5. Create the `ecommerce_db` database by opening a terminal, navigating to the root of the project directory, logging into a mysql shell, and running the following command:

```
source db/schema.sql
```

This will create an empty `ecommerce_db`. At this point you can exit your MySQL shell.

Step 6. Create tables in and seed the `ecommerce_db` by navigating to the root of the project directory in a terminal, and running the following command:

```
npm run seed
```

This will create four tables in the `ecommerce_db`: `category`, `product`, `product_tag`, and `tag`, as well as seed each table with data that can be used for testing the application's API routes.

## Usage

After you have completed the installation steps above, do the following to use the E-Commerce Backend application:

Step 1. Navigate to the root of the project directory in a terminal, and running the following command to start the application server:

```
npm run start
```

You should see the following confirmation that the server is running:

```
App listening on port 3001!
```

Step 2. While the server is running, open your API testing platform and perform CRUD operations on the `ecommerce_db` by hitting the various GET, POST, PUT, and DELETE endpoints defined in the `./routes/api` folder.

For example, the following API endpoints are available to perform CRUD operations on the category data:

```md
# select all categories

GET route at http://localhost:3001/api/categories

# select a single category by id

GET route at http://localhost:3001/api/categories/:id

# create a new category

POST route at http://localhost:3001/api/categories/:id

# update an existing category by id

PUT route at http://localhost:3001/api/categories/:id

# delete an existing category by id

DELETE route at http://localhost:3001/api/categories/:id
```

**Note:** A JSON object with a `category_name` key-value pair MUST be provided in the request body of the above POST and PUT routes for these routes to work. For example:

```json
{
  "category_name": "coffee"
}
```

A similar set of routes is provided to perform CRUD operations on the product and tag data in the database.

Step 4. When you are finished running the application, hit CTRL-C on the keyboard. This will kill the application server and return to a regular terminal prompt.

## Contributing

Contributions to the E-Commerce Backend project are welcome!

The project repo can be forked here: https://github.com/J1741/J1741_e-commerce_backend

## Application Demo

A video demonstrating the application functionality can be viewed here (note this is an unlisted video, so it can ONLY be accessed via the following link):
https://www.youtube.com/watch?v=m8OpHL7DOxU

The following screenshot shows the E-Commerce Backend in use:
![Alt text](./screenshot.png?raw=true "Screenshot of E-Commerce Backend application")

## Questions

Questions and inquiries about the E-Commerce Backend project can be directed to the developer via GitHub: https://github.com/J1741

Or via email: jseventeen41@gmail.com
