# Airbnb Clone Project

## Overview

This is a full-stack clone of the popular accommodation booking platform **AirBnB**. The project aims to provide a fully functional web application where users can browse property listings, view detailed property information, and complete bookings. It covers frontend and backend development, database design, and deployment.

---

## UI/UX Design Planning

### Design Goals

- Create an intuitive booking flow
- Maintain visual consistency across pages
- Ensure fast loading times
- Prioritize mobile responsiveness

### Key Features

- Property search and filtering
- Detailed property view with booking form
- Secure and simple checkout process
- User authentication

### Primary Pages

| Page                 | Description                                                           |
|----------------------|-----------------------------------------------------------------------|
| Property Listing View | Grid display of available properties with filtering options           |
| Listing Detailed View | Detailed property information, image carousel, and booking form       |
| Simple Checkout View  | Streamlined checkout with payment and booking confirmation            |

### Importance of User-Friendly Design

A user-friendly design is essential for a booking system. It minimizes friction in the user journey, improves conversion rates, and increases customer satisfaction. Features like intuitive navigation, clean interfaces, and responsive layouts make the booking process faster and more pleasant for users.

---

### Figma Design Specifications

#### Color Styles

- **Primary:** `#FF5A5F`
- **Secondary:** `#008489`
- **Background:** `#FFFFFF`
- **Text:** `#222222`
- **Secondary Text:** `#717171`

#### Typography

- **Primary Font:** Circular, Medium (500), 16px
- **Headings:** Circular, Bold (700), 24px–32px
- **Secondary Text:** Circular, Book (400), 14px

### Importance of Identifying Design Properties

Identifying design properties (like typography and color styles) in a mockup ensures design consistency across the app. It also speeds up the development process, helps maintain branding, and allows for easier collaboration between designers and developers.

---

## Project Roles and Responsibilities.

| Role               | Responsibilities                                                                 |
|--------------------|-----------------------------------------------------------------------------------|
| Project Manager     | Oversees timeline, coordinates the team, manages deliverables                   |
| Frontend Developers | Build UI components and ensure responsive, consistent design                    |
| Backend Developers  | Develop APIs, manage the database, implement server-side logic                   |
| Designers           | Create UI mockups, define design systems, and ensure good UX                    |
| QA/Testers          | Write test cases, perform thorough testing, and report bugs                     |
| DevOps Engineers    | Manage CI/CD pipelines, deployments, and server infrastructure                  |
| Product Owner       | Define and prioritize features, represent end-users and stakeholders            |
| Scrum Master        | Facilitate agile processes, resolve blockers, and organize sprint activities    |

---

## UI Component Patterns

### Planned Components

- **Navbar**
  - Logo
  - Search bar
  - User navigation
  - Responsive menu
- **Property Card**
  - Property image
  - Basic details (price, location, rating)
  - Favorite (like) button
  - Responsive layout
- **Footer**
  - Site links
  - Company information
  - Social media links
  - Copyright

Each UI component will be reusable and follow the same design principles to maintain consistency across the entire application.



## Team Roles

| Role               | Responsibilities                                                                 |
|--------------------|-----------------------------------------------------------------------------------|
| Project Manager     | Oversees timeline, coordinates the team, manages deliverables                   |
| Frontend Developers | Build UI components and ensure responsive, consistent design                    |
| Backend Developers  | Develop APIs, manage the database, implement server-side logic                   |
| Designers           | Create UI mockups, define design systems, and ensure good UX                    |
| QA/Testers          | Write test cases, perform thorough testing, and report bugs                     |
| DevOps Engineers    | Manage CI/CD pipelines, deployments, and server infrastructure                  |
| Product Owner       | Define and prioritize features, represent end-users and stakeholders            |
| Scrum Master        | Facilitate agile processes, resolve blockers, and organize sprint activities    |

---

## Technology Stack

| Technology     | Purpose                                                              |
|----------------|----------------------------------------------------------------------|
| Django         | Web framework used for building RESTful APIs and backend logic       |
| MySQL          | Relational database to store application data securely               |
| GraphQL        | API query language for efficient data fetching                       |
| Docker         | Containerization tool for environment consistency and deployment     |
| GitHub Actions | CI/CD automation for testing and deployment pipelines                |

---

## Database Design

| Entity     | Fields                                               | Relationships                                     |
|------------|------------------------------------------------------|---------------------------------------------------|
| Users      | id, name, email, password_hash                       | A user can list multiple properties               |
| Properties | id, owner_id, title, description, location           | Each property belongs to one user                 |
| Bookings   | id, property_id, user_id, checkin_date, checkout_date| A booking is linked to a property and a user      |
| Reviews    | id, booking_id, rating, comment                      | Each review is associated with a completed booking|
| Payments   | id, booking_id, amount, payment_status               | Payments are tied to a booking                    |

---

## Feature Breakdown

- **User Management**  
  Enables users to register, log in, and manage profiles securely.  
- **Property Management**  
  Allows users to list properties with images, descriptions, and availability.  
- **Booking System**  
  Users can book properties, view availability, and manage their bookings.  
- **Review System**  
  Enables users to leave reviews after a stay, improving credibility.  
- **Payment Integration**  
  Secure payment processing and confirmation for each booking.  

---
## API Security

| Security Measure         | Explanation                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------|
| **Authentication**       | Ensures that only registered users can access protected routes. Commonly implemented via JWT or OAuth2. |
| **Authorization**        | Determines user permissions (e.g., only property owners can edit listings). Prevents unauthorized actions. |
| **Input Validation**     | Sanitizes incoming data to prevent SQL injection, XSS, and other code injection attacks.      |
| **Rate Limiting**        | Protects APIs from abuse and denial-of-service (DoS) attacks by limiting repeated requests.   |
| **HTTPS Encryption**     | Secures data in transit between the frontend and backend using TLS.                           |
| **Error Handling**       | Avoids leaking sensitive system information through clear and generic error messages.         |


## CI/CD Pipeline

**Objective**: Understand how CI/CD pipelines contribute to the development process.

**Overview**:
CI/CD pipelines automate the process of testing, building, and deploying code. This ensures rapid delivery with minimal human error, maintains consistent environments, and improves overall code quality.

**Tools Used**:
- **GitHub Actions**: For automated testing and deployment triggers.
- **Docker**: Ensures uniform environments across dev, staging, and production.
- **Heroku/AWS**: Deployment platforms for staging and production environments.

---

