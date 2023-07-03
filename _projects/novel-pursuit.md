---
title: 'Novel Pursuit'
subtitle: 'Technologies Used: React.js, Express, Node.js, PSQL, Open Library API'
description: This project involved developing a full-stack web application, designed to facilitate user interaction with a database through a RESTful API. The application adheres to the CRUD (Create, Read, Update, Delete) model.
featured_image: '/images/novel-pursuit/ezgif.com-video-to-gif.gif'
---

## Overview

The goal of this project was to provide an interface that enables users to search for books by title, author, or ISBN using the Open Library API. The back-end integrates user registration and login functionalities, leveraging PostgreSQL for database management. Once registered, users can view, save, and remove books from their personal saved list, called Bookmarks.

See the back-end code in my [Github repository](https://github.com/mlauren77/novel-pursuit-backend) and the front-end code [here](https://github.com/mlauren77/novel-pursuit-frontend)

Below is a GIF demonstrating the mobile version of Novel Pursuit's functionality. It illustrates a user journey: searching for a book by title, adding selected books to their Bookmarks, and finally reviewing and managing their Bookmarks, which includes removing a book.

![novel-pursuit-gif](/images/novel-pursuit/ezgif.com-video-to-gif.gif)

## Axios

Axios is a promise-based HTTP client used for making HTTP requests from both the browser and Node.js environment. It supports a wide range of features like error handling and automatic JSON data transformation. In this project, I used Axios to make HTTP requests to the Open Library API to search for books by title, author, or ISBN.

## Open Library API

For this application, I made extensive use of the Open Library API, an open, editable library catalog that provides APIs for developers to explore its robust book databse. This API gives access to book covers, authors, publication dates, and other significant metadata for millions of books. This vast resource was instrumental in providing rich book data displayed in this application.

You can find the Open Library API documentation at [Open Library](https://openlibrary.org/dev/docs/api/search)

## PostgreSQL

PostgreSQL (PSQL) is an advanced, open-source relational database management system that utilizes SQL to interact with databases. Noted for its robustness, extensibility, and compliance with SQL standards, PSQL is an excellent choice for complex, high-volume applications.

In this project, I incorporated PSQL in the back-end stack to handle user sign-up information, which includes sensitive details like the user's full name, username, password and email. PostgreSQL is used to securely store and retrieve this user data, facilitating smooth, reliable user registration and login processes. 

## Bcrypt

Bcrypt is a password-hashing library designed to secure sensitive user data. It offers additional security measures, such as 'salting' to prevent rainbow table attacks, and adjustable 'work facotrs' to increase the complexity of the hash and hence the resources required to crack it. In this application, I used bcrypt to hash and securely store user passwords in the back-end.

## JWT-Decode

JWT-Decode is a library designed to decode JSON Web Tokens (JWT). JWTs are used for securely transmitting information between parties in the form of a JSON object. They are an essential part of maintaining secure, stateless web applications and can be used to authorize users, maintaining user sessions over multiple requests. In this application, JWT-Decode was employed to facilitate user authentication and maintain user sessions, ensuring a secure and personalized user experience.

## Backend Stack

The back-end was developed using:

* Node.js
* Express
* PostgreSQL

## Frontend Stack

The front-end was developed using:

* React.js
* React-Bootstrap
* React Router
* Axios
* JWT-Decode

## Testing

Testing for both the front-end and the back-end was carried out using:

* Jest
