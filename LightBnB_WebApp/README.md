# LightBnB

## Project Structure

```
├── public
│   ├── index.html
│   ├── javascript
│   │   ├── components 
│   │   │   ├── header.js
│   │   │   ├── login_form.js
│   │   │   ├── new_property_form.js
│   │   │   ├── property_listing.js
│   │   │   ├── property_listings.js
│   │   │   ├── search_form.js
│   │   │   └── signup_form.js
│   │   ├── index.js
│   │   ├── libraries
│   │   ├── network.js
│   │   └── views_manager.js
│   └── styles
├── sass
└── server
  ├── apiRoutes.js
  ├── database.js
  ├── json
  ├── server.js
  └── userRoutes.js
```

* `public` contains all of the HTML, CSS, and client side JavaScript. 
  * `index.html` is the entry point to the application. It's the only html page because this is a single page application.
  * `javascript` contains all of the client side javascript files.
    * `index.js` starts up the application by rendering the listings.
    * `network.js` manages all ajax requests to the server.
    * `views_manager.js` manages which components appear on screen.
    * `components` contains all of the individual html components. They are all created using jQuery.
* `sass` contains all of the sass files. 
* `server` contains all of the server side and database code.
  * `server.js` is the entry point to the application. This connects the routes to the database.
  * `apiRoutes.js` and `userRoutes.js` are responsible for any HTTP requests to `/users/something` or `/api/something`. 
  * `json` is a directory that contains a bunch of dummy data in `.json` files.
  * `database.js` is responsible for all queries to the database. It doesn't currently connect to any database, all it does is return data from `.json` files.

## ERD
!["picture of ERD"](https://github.com/aprilhuang825/LightBnB/blob/master/LightBnB_WebApp/pics/ERD.png)
  
## Getting Started

1. Clone the repository onto your local device.
2. Create a database called lightbnb from the psql terminal.
3. In psql run `\i migrations/01_schema.sql` to create the tables,run `\i seeds/02_seeds.sql` to add data.
4. Install dependencies using the `npm install` command.
5. Start the web server using the `npm run local` command. The app will be served at <http://localhost:3000/>.
6. Go to <http://localhost:3000/> in your browser.

## Dependencies

- Express
- Node 5.10.x or above
- bcrypt
- cookie-session
- body-parser
- nodemon
- pg

## Screenshots

!["Screenshot of my reservations page"](https://github.com/aprilhuang825/LightBnB/blob/master/LightBnB_WebApp/pics/My%20reservations.png)
!["Screenshot of create listing page"](https://github.com/aprilhuang825/LightBnB/blob/master/LightBnB_WebApp/pics/Create%20Listing.png)
!["Screenshot search page"](https://github.com/aprilhuang825/LightBnB/blob/master/LightBnB_WebApp/pics/Search%20page.png)