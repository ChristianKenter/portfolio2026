---
title: "Authentication, JWT and User Roles"
date: 2026-10-02T09:00:00+02:00
draft: false
weight: 5
---

This week I focused on authentication and security in MyOllama.

I worked on the login functionality and the use of JSON Web Tokens. After a successful login, the application can issue a JWT that the client can use when accessing protected endpoints.

The API uses Bearer tokens in the Authorization header, while the website flow can also use an HTTP-only authentication cookie.

I also worked with role-based access control. The project defines three roles: ANYONE, STANDARD and PREMIUM. These roles make it possible to restrict certain endpoints depending on the user's permissions.

For example, video generation requires an authenticated standard-level user, while premium users can access standard-level functionality as well.

One important thing I learned is that authentication and authorisation are two separate concerns. First the application needs to establish who the user is, and then it needs to check whether that user is allowed to perform the requested action.

Next week I will focus on connecting Ollama and generating quiz questions.
