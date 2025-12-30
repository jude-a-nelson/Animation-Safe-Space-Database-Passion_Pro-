📘 Animation Safe Space Database (ASSDB)
Project Overview

The Animation Safe Space Database (ASSDB) is a 3-tier web application designed to explore and implement master–detail (one-to-many) database relationships using a RESTful architecture. The project focuses on organizing animation content in a way that helps users, particularly parents and educators to identify appropriate animated media based on age group, content warnings, and purpose (entertainment vs. education).

This project builds upon foundational concepts introduced in the ListDetails / Ones-to-Many assignment and expands them to a richer, real-world domain.

Problem Statement

A common misconception is that all animation is intended for children. In practice, animated content spans a wide range of age groups and themes, including material that may be inappropriate for younger audiences. Without clear classification, users may unintentionally expose children to violent, sexual, or otherwise mature content.

The ASSDB addresses this issue by providing a structured database that classifies animations by studio, age group, genre, and content warnings, while also supporting community interaction features such as comments, ratings, and moderation.

Solution Summary

The ASSDB is implemented as a (master detail) database system:

Studio acts as the master entity

Animation acts as the detail entity

Additional feature entities (Comments, Ratings, Fan Art, Reports) extend functionality without overcomplicating the core schema

The system is designed to be expandable, allowing future features such as user authentication, independent artist uploads, and recommendation engines to be added later.

Current Features (Implemented Scope)

Studio and Animation data management (CRUD)

One-to-Many relationship between Studios and Animations

Age group classification (e.g., All Ages, 7+, 16+, 18+)

Genre and animation type classification

Commenting on animations (anonymous for now)

Rating animations (1–6 scale)

Fan art uploads (moderated)

Reporting system for inappropriate content

Seeded data for realistic demonstrations

Search and filtering logic (service-level design)

Note: User accounts and authentication are intentionally excluded from the current scope per assignment requirements.

Planned / Future Features

These features are intentionally deferred to later phases:

User accounts and authentication

Independent artist animation uploads

Recommendation engine based on ratings and viewing patterns

Advanced moderation dashboards

Custom user profiles and saved preferences

Animated or customizable UI backgrounds

Database Design
Core Entities
Studio (Master)

Represents animation studios

Can exist independently

Produces multiple animations

Animation (Detail)

Represents individual animated films or series

Cannot exist without a parent studio

Stores classification and availability metadata

Supporting Feature Entities

Comment – user feedback tied to an animation

Rating – numeric evaluation of an animation

FanArt – community-submitted artwork

Report – moderation mechanism for unsafe content

UML Design

The project UML includes:

Entity relationships (Studio → Animation)

Feature relationships (Animation → Comments, Ratings, Fan Art)

Service level components (Search, Classification, Moderation)

This separation ensures clarity between data storage and system behavior, following best practices in software design.

Seed Data

The database includes synthetic seed data representing:

Multiple studios (e.g., Studio Ghibli, Pixar, MAPPA)

A mix of child-safe and mature animations

Realistic ratings, comments, and moderation cases

Seed data is used to:

Demonstrate relational integrity

Validate classification logic

Support testing and presentation

Tech Stack

Backend: Python (FastAPI or Flask)

Database: SQLite / PostgreSQL

Architecture: 3-Tier (Client → REST API → Database)

Frontend (later phases):

Vanilla JavaScript

React

Project Phases
Phase 1 – Planning & Design

Define project scope

Design database schema

Create UML diagrams

Generate SQL schema and seed data

Phase 2 – Backend Development

Implement REST API

CRUD operations for all entities

One-to-Many relationship endpoints

API testing with Postman / Insomnia

Phase 3 – Frontend Integration

Vanilla JavaScript UI

React UI

Dynamic display of relational data

Kanban Workflow

Development tasks are broken into:

Database tasks

API tasks

Feature tasks

Testing and documentation tasks

Each task includes subtasks to ensure incremental progress and clear milestones.

Educational Goals

This project demonstrates understanding of:

Relational database design

Master detail (one-to-many) relationships

RESTful API architecture

Data classification and safety considerations

Scalable and maintainable system design

Conclusion

The Animation Safe Space Database provides a structured, scalable approach to organizing animation content while prioritizing user safety and clarity. By combining solid database fundamentals with thoughtful feature planning, the project serves both as an academic exercise and a foundation for future expansion.
