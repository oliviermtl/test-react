# Speedoc - React Front test

This test is a part of our hiring process at Speedoc for frontend positions. It should take you between less than 6 hours depending on your experience.

## Summary

The goal of this test is to make you code a small ReactJS app. We have prepared a skeleton app for you, but please change whatever you want (CSS files, HTML structure, JS structure...).

You should use Hooks, functionnal components, custom scss (no boostrap or other UI libraries) and no Redux.

What is expected :

### Login :

  1. Create simple page to login with those fields :
     - Email
     - Secret Key
     - Password
     - Remember me checkbox
  2. Call the Login service from api
  3. Keep informations from login

  To Test :

  - email : `jarvis@speedoc.com`
  - password : `speedocdemo`
  - secret key : `Mitrfd3Ev45e3tvzmOYeT7HdMe4jGEpN5rawgNGM`

**Bonus** : Make those fields required with patterns

![Login Page Example](/src/images/login.jpg)

### Home Page :
  > If the user is logged, he can access to this page

1. Search User :

- Create input to search an user by calling the api service.
- The search action will be triggered with a button

2. User form :
   > If a user is found, pre-fill the form

- The form will contains this fields :
  - Full Name
  - Email
  - Birthdate
  - Gender (Select with Values = ["Male" , "Female"])
  - Phone Extension (ex : +65)
  - phone Number

Show us what you can do in 6 hours top :) Don't spend too much time on designing your app.

![User Form Example](/src/images/form.jpg)

## Installation

We're using [npm](https://www.npmjs.com/) here:

```
npm install
npm start
```

## API documentation

You will find an exemple of how to use our api in the file **authenticationService.js**.

**IMPORTANT** : Look at the `httpService.js` file to understand how to call the service.
The `key` or `x-api-key` in the request header is the secret key of the login page, and the `jwt` is obtained by calling the login service.

Header :

```
accept: application/json, text/plain, */*
accept-encoding: gzip, deflate, br
accept-language: fr-FR,fr;q=0.9,en-US;q=0.8,en;q=0.7,es;q=0.6,it;q=0.5,de;q=0.4
//authorization:
x-api-key: Mitrfd3Ev45e3tvzmOYeT7HdMe4jGEpN5rawgNGM

```

### Routes

- **Login** - https://dev.api-rest.speedoc.com/session/login : Post datas to log into the app.

Body :

```
{
  "password" : "1team@speedoc",
  "username": "dummy@speedoc.com",
  "rememberMe": true
}
```

- **Search** - https://dev.api-rest.speedoc.com/user/search?term=tan : Get search an existing user (ex: tan or test). If you have multiple users in the response just take the first one.

## Submission

Fork this repository and send us a pull request. We'll review it and get back to you in order to talk about your code!
