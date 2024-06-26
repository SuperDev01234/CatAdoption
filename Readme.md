# Requirements

## Objective

Develop a RESTful API with NestJS framework for a cat adoption agency. The API will manage cat profiles, and user interactions.

## Key Features

- Cat Profiles: Create, read, update, and delete profiles for cats available for adoption.
- User Authentication: Secure user registration and login functionality.

## Technical Specifications:

- Use blockchain network as database
- Utilize Passport.js for user authentication with JWT tokens.
- Apply class-validator and class-transformer for input validation and serialization.

## Endpoints to Implement:

- POST /auth/register: Register a new user.
- POST /auth/login: Authenticate a user and return a JWT.
- GET /cats: Retrieve a list of all cats.
- POST /cats: Create a new cat profile.
- GET /cats/{id}: Retrieve a cat profile by ID.
- PUT /cats/{id}: Update a cat profile by ID (admin only).
- DELETE /cats/{id}: Delete a cat profile by ID (admin only).

## UI Implementation:

Build an API simulator like Postman (:come up with your own design)

- User should be able to input API URL
- User should be able to input HTTP header information
- User should be able to input HTTP body information
- User should be able to call the API and display the result in the UI

# Environment Setup

Used mono-repo for configuring this repository

## 1. Frontend

### Main Tech-Stack

- Primary: Vite(React)
- Styling: Tailwind CSS
- Package Manager: NPM

### Setup Instruction

- Installing Dependencies

```
npm install
```

- Running Dev Server

```
npm run dev
```

- Find `http://localhost:5173` to run the frontend application.

## 2. Backend

### Main Tech-Stack

- Primary: NestJS
- Extra
  - bcrpyt: Password hashing
  - jsonwebtoken: JWT generation
  - passport, passport-jwt: Authentication with JWT
- Package Manager: NPM

### Setup instruction

- Copy `.env` and rename it as `.env.local`.

- Fill in each variables with appropriate values.

- Copy `Cat.json` and `User.json` file in `Solidity_SmatContract` to `NestJS_Backend/src/Contract`.

- Installing Dependencies

```
npm install
```

- Running Dev Server

```
npm run start:dev
```

- Find `http://localhost:3000` to run the backend application.

## 3. Smart Contracts

### Main Tech-Stack

- Primary: Solidity

### Setup instruction

- Setup `Ganache`
- Setup Truffle by using `npm i -g truffle`
- Compile the contracts

```
truffle compile
```

- Implement Migration

```
truffle migrate --reset
```

# Challenges

- Writing to smart contracts for managing the data related to User and Cats.
  By taking a look at and following the tutorial reference for writing down the contracts and integrating them using Web3.js, I could get the understandings of how smart contracts work.

# Things can be improved

- Smart contracts just returns the array as the data.
  If I can define some data pipelines or clear type schemas, I can make my application more type-safe.

# Screenshot

![screenshot](./screenshot.png)
