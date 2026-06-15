# Web Project Portfolio Website

A professional personal portfolio website built with **PHP, MySQL, HTML, CSS, and JavaScript**.  
This project presents profile information, skills, projects, social links, and a functional contact and authentication flow.

## Overview

This website is designed to showcase a developer profile in a clean, responsive, and interactive way.  
It includes:

- A modern portfolio landing page
- Skills and project showcase sections
- Social and contact integration
- Contact form submission to MySQL
- User signup and login pages

## Key Features

- **Responsive navigation** with desktop and hamburger mobile menu
- **Portfolio sections**: About, Experience, Projects, Contact
- **Interactive UI effects**: animations, hover effects, stylized social links
- **Contact form backend** with PHP + MySQL insert operation
- **Authentication flow**:
  - Sign up with duplicate-username check
  - Login using stored credentials
- **Asset-based presentation** (profile images, project previews, downloadable CV)

## Modern Technologies Used

- **Frontend**
  - HTML5
  - CSS3 (custom styling + media queries)
  - Vanilla JavaScript
  - Font Awesome (icons)
  - Google Fonts (Poppins)

- **Backend**
  - PHP (server-side scripting)
  - MySQL (data storage via `mysqli`)

## Project Structure

```text
Web_Project/
├── index.php            # Main portfolio page + contact form handler
├── login.php            # User login page + login validation
├── signup.php           # User registration page + user creation
├── script.js            # Menu toggle and client-side interactions
├── style.css            # Main styles
├── mediaqueries.css     # Responsive breakpoints
├── contactUs.css        # Contact section styles
├── login.css            # Login/signup page styles
├── submit.css           # Additional button styles
└── assets/              # Images and resume
```

## Setup & Installation

### 1) Prerequisites

- PHP 7.4+ (or newer)
- MySQL Server
- Local server stack (XAMPP/WAMP/LAMP) or PHP built-in server

### 2) Clone the repository

```bash
git clone https://github.com/Sohelkhan26/Web_Project.git
cd Web_Project
```

### 3) Configure database

Create a MySQL database named:

```sql
message
```

Create required tables:

```sql
CREATE TABLE login (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(255) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL
);

CREATE TABLE table1 (
  id INT AUTO_INCREMENT PRIMARY KEY,
  fullName VARCHAR(255) NOT NULL,
  email VARCHAR(255) NOT NULL,
  message TEXT NOT NULL
);
```

### 4) Update DB connection if needed

Current code expects:

- Host: `localhost:3308`
- Username: `root`
- Password: empty
- Database: `message`

If your environment differs, update connection values in:

- `index.php`
- `login.php`
- `signup.php`

### 5) Run the project

Place the project inside your local server root (e.g., `htdocs`) and open:

```text
http://localhost/Web_Project/index.php
```

## Usage

- Open **Home** page to view profile, skills, and projects.
- Use **Login** button in the top navigation to access auth pages.
- Use **Signup** to register a new user.
- Use **Login** to authenticate.
- Submit the **Contact Me** form to store messages in the database.

## Professional Highlights

- Clean sectioned portfolio layout suitable for personal branding
- Responsive design for desktop and mobile
- End-to-end basic web app flow (UI + backend + database)
- Ready to showcase in CV/portfolio as a full-stack beginner-to-intermediate project

## Security & Improvement Notes

This project is functional and portfolio-ready; for production-grade deployment, consider:

- Using prepared statements to prevent SQL injection
- Hashing passwords with `password_hash()` / `password_verify()`
- Adding form validation and sanitization
- Introducing session-based authentication
- Adding CSRF protection and rate limiting

## Future Enhancements

- Admin panel to manage contact messages
- Project management dashboard (add/edit/delete projects)
- Email notifications for contact submissions
- Profile content management from database
- Deployment with CI/CD and environment-based configuration

## Author

**Md Shahrukh Khan Sohel**  
GitHub: [@Sohelkhan26](https://github.com/Sohelkhan26)

