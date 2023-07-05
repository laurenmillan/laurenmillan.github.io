---
title: 'Jobly'
subtitle: 'Technologies Used: React.js, Express, Node.js, PSQL'
description: Jobly is a dynamic full-stack job posting web application. It allows users to search and apply for jobs of their interest and features a comprehensive component hierarchy, a functional database, and RESTful routing. Additionally, Jobly supports robust user authentication and profile management.
featured_image: '/images/jobly/jobly.gif'
---

## Overview

Jobly is a robust full-stack web application, designed to emulate a real-world job posting platform. It boasts a comprehensive component hierarchy, a functional database, RESTful routing, and leverages an API helper for seamless backend interactions. The application also provides user authentication and profile editing capabilities, empowering users to browse and apply to an extensive list of companies and job postings. A key feature of Jobly is its user-first design approach, requiring users to sign up before they can start applying to jobs.

See the code in my [Github repository](https://github.com/mlauren77/Jobly/tree/deploy)

Below is a GIF demonstrating the mobile version of Jobly's functionality.  It traces the journey of a user from using the live search feature to look for companies by name, navigating through the list of available jobs, to finally applying to a selected job.

![jobly-gif](/images/jobly/jobly.gif){:width="250px"}

## Axios

Axios is a promise-based HTTP client used for making HTTP requests from both the browser and Node.js environment. In this project, Axios is utilized to interact with the Jobly API to search for companies and jobs, filter results by name or title, and handle user job applications.

Key features of Axios, such as error handling and automatic JSON data transformation, significantly enhance the reliability and ease of data handling in the application. For instance, a user can apply to a job by sending a POST request to the API through Axios. This request indicates that a user, identified by a specific username, is applying for a job associated with a particular id.

By leveraging Axios, this project ensures efficient communication with the back-end, fostering a seamless user experience in job search and application processes. 

## PostgreSQL

PostgreSQL (PSQL) is a robust, extensible, and SQL standards-compliant open-source relational database management system. It is widely adopted for complex, high-volume applications due to its advanced capabilities and strong data integrity enforcement.

In this project, PostgreSQL serves as the main database management system in the back-end, responsible for storing, retrieving, and managing data related to user accounts and job postings. It securely stores sensitive user information including full name, username, password, and email, facilitating reliable user registration and login processes. 

Furthermore, PostgreSQL interacts with the 'Company' and 'Job' models in the application. These models act as an interface between the application and the PSQL database, allowing the application to manage and interact with data in the 'companies' and 'jobs' tables in the database. The 'Company' model, for instance, includes methods for creating, reading, updating, and deleting companies, while the 'Job' model offers similar functionalities for job postings. This structured data interaction enables a smooth and efficient flow of data in the application, resulting in a seamless user experience.

## Bcrypt

Bcrypt is a password-hashing library designed to secure sensitive user data. It offers additional security measures, such as 'salting' to prevent rainbow table attacks, and adjustable 'work factors' to increase the complexity of the hash and hence the resources required to crack it. In this application, I used bcrypt to hash and securely store user passwords in the back-end.

## Middleware

In the back-end of the application, middleware is utilized to handle common authentication scenarios across routes. The implemented middleware functions are crucial in maintaining the security of the application, ensuring that only authenticated users can access specific routes and that user privileges are properly enforced. This way, unauthorized access is prevented, which is essential for protecting sensitive data and ensuring the application functions as intended.

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

Unit testing for the back-end of the application was performed using Jest, which involves testing individual pieces of software to ensure they successfully work as expected under a variety of conditions. This included testing various authentication and authorization middleware functions in isolation, ensuring that they handle differenct scenarios properly. 

Additional testing included testing the back-end routes for companies, jobs, and users using the Supertest library to simulate HTTP requests to the API and checks if the responses are as expected. The tests are performed on various CRUD (Create, Read, Update, Delete) operations that the API should be able to perform.

* Jest
* Supertest
