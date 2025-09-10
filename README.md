# airbnb-clone-project
## 👥 Team Roles
1. Backend Developer: Responsible for implementing API endpoints, database schemas, and business logic.
2. Database Administrator: Manages database design, indexing, and optimizations.
3. DevOps Engineer: Handles deployment, monitoring, and scaling of the backend services.
4. QA Engineer: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## ⚙️ Technology Stack
1. Django: A high-level Python web framework used for building the RESTful API.
2. Django REST Framework: Provides tools for creating and managing RESTful APIs.
3. PostgreSQL: A powerful relational database used for data storage.
4. GraphQL: Allows for flexible and efficient querying of data.
5. Celery: For handling asynchronous tasks such as sending notifications or processing payments.
6. Redis: Used for caching and session management.
7. Docker: Containerization tool for consistent development and deployment environments.
8. CI/CD Pipelines: Automated pipelines for testing and deploying code changes.

## 🗄️ Database Design
Key Entities
1. Users
- id: Primary key
- name: Full name
- email: Unique email address
- password: Hashed password
- role: User role (guest/host/admin)

2. Properties
- id: Primary key
- user_id: Foreign key → Users (host who owns the property)
- title: Property title
- description: Property details
- price_per_night: Price of booking

3. Bookings
- id: Primary key
- user_id: Foreign key → Users (guest who booked)
- property_id: Foreign key → Properties
- check_in: Start date
- check_out: End date

4. Payments
- id: Primary key
- booking_id: Foreign key → Bookings
- amount: Payment amount
- status: Payment status (pending/completed)
- transaction_date: Date of payment

5. Reviews
- id: Primary key
- user_id: Foreign key → Users (who posted the review)
- property_id: Foreign key → Properties
- rating: Rating out of 5
- comment: Review text

6. Relationships
- A User can own multiple Properties.
- A Booking belongs to one User and one Property.
- A Payment is tied to a Booking.
- A Review belongs to both a User and a Property.
  
