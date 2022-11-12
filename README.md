# Secrets-Google-Auth
<h3>This is a Secrets confession website, where a user can tell their secrets while being anonymous.</h3>
This was a personal project undertaken to learn google Auth, and mongodb.

<br>

## Tech Stack
- Javascript
- Node js
- MongoDB
- Mongoose
- Google O2.Auth

<br>


## MongoDB schema
```
  email: String,
  password: String,
  googleId: String,
  secret: String,
```

<br>

## How does the site work?
### Register
The user will first have to register using either email and password or using <b>Google Sign-in</b>.<br>
- For Google Sign in, we have used O2.Auth. We first sign in the user using their prefered email id, and then store the googleID in the local MongoDB.<br>

For normal email and password, the password is hashed and then stored locally in MongoBD
<br>

### Login
For Login, the user can either enter email / username and password they set, which will then be verified from the backend
- For Google Sign in, we first login the user from google, and then verify if the user has already registered or not from our local database.<br>
<br>

### Adding Secrets
We store the secrets for each user in the secret variable of each user, inside our database.<br>
<br>

### Accessing Secrets
Since secrets are anonymous, and can be seen by everyone.<br>
We find all the secrets of the user that are their and present it to every user, while keeping everyone anonymous.

<br><br>

## What I learned
- I learned the six levels of Authentication, from the very weak to the very strongsts available
    - Level 1: 