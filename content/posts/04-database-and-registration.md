---
title: "Database Setup and User Registration"
date: 2026-09-25T09:00:00+02:00
draft: false
weight: 4
---

This week I focused on the database and user registration functionality.

I worked with PostgreSQL and Hibernate to establish the persistence layer and organise how client information is stored. The Client entity is central to this part of the application because users need an account before accessing protected functionality.

I also worked on registration validation. The application needs to reject invalid usernames, passwords that are too short and usernames that already exist in the database.

An important part of this work was password security. Instead of storing passwords as plain text, I used BCrypt to hash them before saving them.

I also looked at the difference between the website registration flow and the JSON API registration flow. They have different request formats, so it is important that both are handled consistently.

The registration foundation is now clearer. Next week I will focus on login, authentication tokens and access control.
