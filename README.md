# Bookflix

Group 2 – Una Cristiano Machado University

## About the Project

Bookflix (a fictional name) is a mobile application designed to support users in developing the habit of reading literary works.
It allows readers to access personalised reading plans based on their preferred genres.

Gamification concepts are applied to make the reading experience more dynamic and engaging, rewarding users with points based on their performance.

---

## Sustainable Development Goals

The Bookflix project aligns with **SDG 4 – Quality Education**. Our proposal contributes to this goal by promoting continuous opportunities to develop strong reading habits.

By gamifying reading, we aim to encourage users to read more frequently and for longer periods, which we consider essential for quality education. Reading books enables individuals—especially those in developmental stages—to learn new concepts, expand their vocabulary, and deepen their understanding of literature and the arts.

---

## Architecture

The application follows a **microservices-oriented architecture**. It consists of a Flutter (Dart) frontend and a Node.js backend, with PostgreSQL as the database.

### Frontend

The Dart programming language is used via the Flutter framework to build the mobile application, enabling the creation of user interfaces through widgets.

Logic related to data handling is partially managed on the frontend, including form sanitisation and email structure validation.

**Example project structure:**

* `main.dart`: Main entry point of the application
* `componentes.dart`: Custom and reusable widgets
* `funcoes.dart`: Abstraction of functions used in application logic
* `'page'.dart`: UI pages, each representing a route within the framework

> The Flutter frontend is responsible for the user interface and represents the **Presentation Layer**.

---

### Backend

The backend uses the Express framework (Node.js) to create an HTTP server that manages application routes and handles RESTful HTTPS requests.

**PostgreSQL Database:**
Used for storing persistent data, including user information, reading plans, and books. Sensitive data such as passwords are encrypted using the Bcrypt library, adding a security layer. Basic user validation is performed via email and password.

> The Node.js backend is responsible for processing data sent and requested by the frontend, representing the **Business Logic Layer**.
> It is worth noting that parts of the frontend may also take on characteristics of this layer due to data handling responsibilities.
> The **Data Persistence Layer** is represented by the PostgreSQL database, responsible for storing and managing application data.

---

### Basic Data Flow

Example of a typical operation:

1. **Authentication:**
   1.1 The user enters email and password in form fields
   1.2 The frontend validates and sanitises the input
   1.3 The frontend sends a POST request to the backend login route
   1.4 The backend receives the request and verifies credentials
   1.5 The backend returns a response
   1.6 The frontend stores the response in a global variable for use
   1.7 The global variable is cleared when the application is closed

---

## Prototype Screens Overview

*(The actual prototype may change during development)*

The user begins by creating an account via the registration page, accessible from the login screen.

<figure> <img src="https://drive.google.com/uc?export=view&id=1bMoGaf9mxiWhVBeMIEIg5VQWQ8gDjlfh" width="150" alt="Página de Cadastro"> <figcaption>(Registration Page)</figcaption> </figure>
<br>
<figure> <img src="https://drive.google.com/uc?export=view&id=1W4NhoyNJcSB5_-4U-qHKxAPwJBaAnA4z" width="150" alt="Página de Login"> <figcaption>(Login Screen)</figcaption> </figure>

---

After the first login, a brief introduction is displayed to help the user understand how to start using the app.

<figure> <img src="https://drive.google.com/uc?export=view&id=1DlWTTZ1oxVkHiWvRh-JMZpDtqJkASBWZ" width="150" alt="Introdução"> <figcaption>(Introduction)</figcaption> </figure>

---

The user is then redirected to the main page. If no reading plan is active, no reading data will be displayed.

<figure> <img src="https://drive.google.com/uc?export=view&id=1Oq9KS2ZxJWRh74gRpcRFD7vfr1LcFG_j" width="150" alt="Página Principal (vazia)"> <figcaption>(Main Page [empty])</figcaption> </figure>

---

After selecting three preferred literary genres (as guided), the user chooses one of the suggested reading plans.

In the future, functionality will be added to search for and include specific books in a custom plan. Each plan consists of nine books to be read within a defined timeframe.

<figure> <img src="https://drive.google.com/uc?export=view&id=1p3sx-0FcYwfx17jbxDrZ96QvGiVv0vns" width="150" alt="Escolha de Roteiros"> <figcaption>(Reading Plan Selection)</figcaption> </figure>

---

Once selected, the plan becomes active. The user can begin reading according to it.

To earn points, each book must be completed within a specified period. The user may read only one book at a time, following the active plan.

<figure> <img src="https://drive.google.com/uc?export=view&id=1eDffogU6YnhqyH2NRP7ZQuDwm8OO48IA" width="150" alt="Roteiro Vigente"> <figcaption>(Active Reading Plan)</figcaption> </figure>

---

The user then starts a reading session. A timer is used to track and record reading activity.

*(In future versions, an eBook reader with automated tracking should be implemented.)*

<figure> <img src="https://drive.google.com/uc?export=view&id=1PIbcm3YHZvKsoP4Hh1d3SYOLH76YGHXy" width="150" alt="Roteiro Vigente"> <figcaption>(Session Tracking)</figcaption> </figure>

---

At the end of a session, the user enters the last page read to complete it.

*(Once the eBook reader is implemented, the user will only need to confirm the session end, and the system will handle tracking automatically.)*

<figure> <img src="https://drive.google.com/uc?export=view&id=1d4ib1C8-nZf2bHZLuXHIR0gCXByK-XL3" width="150" alt="Roteiro Vigente"> <figcaption>(End of Reading Session)</figcaption> </figure>

---

Information regarding reading progress is displayed in the user profile, and completed books are stored in the user’s history.

<figure> <img src="https://drive.google.com/uc?export=view&id=1QjTmI0m9tanj9DV6vkjxqZc-3dStkR7c" width="150" alt="Roteiro Vigente"> <figcaption>(Main Page [with progress])</figcaption> </figure>
<figure> <img src="https://drive.google.com/uc?export=view&id=1k-awqIbiBflZkhTz2G9VcSNrpp5n5AIa" width="150" alt="Roteiro Vigente"> <figcaption>(Reading History)</figcaption> </figure>

---

Users can update their account details through the profile settings.

<figure> <img src="https://drive.google.com/uc?export=view&id=1Gpy3k9NDnp0fKoK8yKexKfuv73h0Jjsi" width="150" alt="Roteiro Vigente"> <figcaption>(Dropdown Menu)</figcaption> </figure>
<figure> <img src="https://drive.google.com/uc?export=view&id=1HUxkv8xx-g8qnjrhz3jA33BmFPZ08kcV" width="150" alt="Roteiro Vigente"> <figcaption>(Profile Editing)</figcaption> </figure>

---

## Future Improvements

A reward shop is planned, where users will be able to exchange points for badges to enhance their profile and share achievements on social media.
