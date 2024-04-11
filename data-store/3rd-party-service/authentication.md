---
title: Authentication
tags:
  - TechSkills
DateStarted: 2023-03-06
DateModified: 2023-12-02
status:
---

## What

Different from authorization

#### 1. Authentication

the process of identifying an individual, eg. User login and you validate their identity

#### 2. Authorization

pertains to the permission that individual has, eg. a logged in user can't do whatever they want and go to admin areas and start editing content

## How to implement

#### 1. Sessions & [Cookies](Cookies)

- Server maintains session and ID stored in cookie

#### 2. JSON web tokens

- Token is stored and sent to protected routes

#### 3. OAuth

- Open standard to use 3rd-party services

#### 4. Third Party Services

- Auth0, Okta, AWS Cognito, Firebase

#### 5. Other Topics

- Password hashing
- Two-factor auth
- Protecting routes
