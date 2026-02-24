# INFO3180 - Lab 2
## Gavin Seaton - 620043505

A Flask web application built for the INFO3180 course. This project demonstrates routing, templating, static file management, and dynamic content rendering.

## Features

- User profile page with formatted date information
- Responsive design with Bootstrap styling
- Static file management (CSS, JavaScript, images)
- Jinja2 templating engine integration

## Setup Instructions

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Installation

1. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   ```

2. **Activate the virtual environment:**
   
   **On macOS/Linux:**
   ```bash
   source venv/bin/activate
   ```
   
   **On Windows:**
   ```bash
   .\venv\Scripts\activate
   ```

3. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask development server:**
   ```bash
   flask --app app --debug run
   ```

   The application will be available at `http://localhost:5000`

## Project Structure

```
info3180-lab2/
│
├── app/
│   ├── __init__.py           # Flask app initialization
│   ├── views.py              # Route handlers and template functions
│   ├── static/
│   │   ├── css/
│   │   │   ├── app.css       # Custom styles
│   │   │   └── bootstrap.min.css
│   │   ├── js/
│   │   │   ├── app.js        # Custom JavaScript
│   │   │   └── bootstrap.bundle.min.js
│   │   └── photos/
│   │       └── my_photo.jpg  # User profile photo
│   └── templates/
│       ├── base.html         # Base template
│       ├── header.html       # Navigation header
│       ├── footer.html       # Footer component
│       ├── home.html         # Home page
│       ├── about.html        # About page
│       ├── profile.html      # User profile page
│       └── 404.html          # Error page
│
├── requirements.txt          # Python package dependencies
├── README.md                 # This file
└── .gitignore               # Git ignore rules
```

## Available Routes

- `/` - Home page
- `/about/` - About page
- `/profile/` - User profile page (displays formatted join date)



### Date Formatting
The `format_date_joined()` function in `views.py` formats dates as "Mon, YYYY" (e.g., "Feb, 2026"). It's made available to all templates via a Flask context processor.

