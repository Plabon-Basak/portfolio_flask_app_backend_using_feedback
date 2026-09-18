# Portfolio Website â€” Flask Backend with Feedback

A personal **portfolio website** built with Flask. Beyond a clean landing page,
it includes a working **contact form** that stores visitor feedback to a JSON
file, plus an admin-style page for viewing every submission.

![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Flask](https://img.shields.io/badge/Flask-2.x-000000)
![HTML/CSS/JS](https://img.shields.io/badge/HTML%2FCSS%2FJS-frontend-orange)

## Features

- Landing page with hero, about, skills, and projects sections
- **Contact form** that saves name, email, and message to `feedback.json`
- **Feedback page** listing all submissions
- Success confirmation after a form is submitted
- Fully styled with custom CSS and a small bit of JavaScript

## Routes

| Route              | Method(s)          | Description                          |
|--------------------|--------------------|--------------------------------------|
| `/`                | GET                | Portfolio home page                  |
| `/contact`         | GET                | Contact / feedback form              |
| `/submit-feedback` | POST               | Saves feedback and redirects         |
| `/feedback`        | GET                | Lists all feedback submissions       |

## Getting Started

### Requirements

Install Flask:

```bash
pip install flask
```

### Run the app

```bash
python portfolio_website/app.py
```

Then open **http://127.0.0.1:5000** in your browser.

## Feedback storage

Feedback is appended to `portfolio_website/feedback.json` in this shape:

```json
[
  {
    "name": "Jane Doe",
    "email": "jane@example.com",
    "message": "Great portfolio!"
  }
]
```

## Project structure

```
portfolio_flask_app_backend_using_feedback/
â”œâ”€â”€ portfolio_website/
â”‚   â”œâ”€â”€ app.py            # Flask application
â”‚   â”œâ”€â”€ feedback.json     # Stored feedback
â”‚   â””â”€â”€ templates/        # HTML templates
â”‚       â”œâ”€â”€ index.html
â”‚       â”œâ”€â”€ contact.html
â”‚       â””â”€â”€ feedback.html
â”œâ”€â”€ css/style.css         # Styles
â””â”€â”€ js/script.js          # Frontend behavior
```

## License

This project is open-source and available under the [MIT License](LICENSE).