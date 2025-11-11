# Django-Project-1: Game Company Website

## Overview

**Django-Project-1** is a full-stack web application built using the Django framework, designed as a dynamic website for a fictional game development company. This project serves as an excellent portfolio piece or a customizable template for creating professional websites in the gaming industry. It demonstrates key Django concepts like models, views, templates, and admin interfaces, while incorporating frontend enhancements for a polished user experience.

The site focuses on showcasing games, company news, team profiles, and user interactions, making it ideal for indie game studios or hobbyist developers. Built with responsiveness in mind, it works seamlessly on desktops, tablets, and mobiles. This project is perfect for beginners transitioning from basic Python to web development, as it includes well-commented code, modular structure, and real-world features.

If you're learning Django, use this as a starter kit: fork it, customize the content, and deploy it to platforms like Heroku or Vercel. The codebase emphasizes clean architecture, security best practices (e.g., CSRF protection), and scalability.

## Key Features

- **Dynamic Homepage**: A visually appealing landing page with carousels for featured games, latest news teasers, and company highlights. Content is dynamically fetched from the database for easy updates.
  
- **Game Catalog**: Browse and detail pages for games, including:
  - Descriptions, genres, and release dates.
  - Embedded trailers (YouTube/Vimeo integration).
  - Screenshots gallery with lightbox effects.
  - Download or purchase links (external or simulated).

- **News and Blog System**: A fully functional blog module with:
  - Post creation via Django admin.
  - Categories, tags, and search functionality.
  - Pagination for long lists.
  - Comment system (moderated for spam prevention).

- **Team and About Pages**: Showcase company info and team members with:
  - Bios, profile photos, and social media links (LinkedIn, Twitter/X, GitHub).
  - Interactive hover effects for engagement.

- **Contact Form**: User-friendly form for inquiries, integrated with email backend (configurable for SMTP like Gmail).
  
- **User Authentication**: Basic login/register system for admins or users, with role-based access (e.g., only admins post news).
  
- **Admin Dashboard**: Customized Django admin panel for managing content, with inline editing and filters.
  
- **Responsive Design**: Built with Bootstrap 5 for mobile-first layouts, ensuring accessibility across devices.
  
- **SEO and Performance**: Meta tags for search engines, lazy loading for images, and basic caching for faster load times.

## Tech Stack

- **Backend**: Django 4.x (Python 3.10+)
- **Frontend**: HTML5, CSS3, JavaScript (ES6), Bootstrap 5
- **Database**: SQLite (default; easily switchable to PostgreSQL or MySQL)
- **Other Libraries**:
  - Django Crispy Forms for form rendering.
  - Pillow for image processing (e.g., thumbnails).
  - Django-ckeditor for rich text editing in blogs.
- **Deployment Tools**: Gunicorn + Nginx (recommended for production), or Heroku for quick setup.

## Installation

Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```
   git clone https://github.com/waratecs123/Django-Project-1.git
   cd Django-Project-1
   ```

2. **Create a Virtual Environment**:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```
   pip install -r requirements.txt
   ```

4. **Set Up Environment Variables** (optional for production):
   - Create a `.env` file in the root directory.
   - Add keys like `SECRET_KEY=your_secret_key`, `DEBUG=False`, `EMAIL_HOST_USER=your_email`.

5. **Apply Migrations and Create Superuser**:
   ```
   python manage.py makemigrations
   python manage.py migrate
   python manage.py createsuperuser
   ```

6. **Run the Development Server**:
   ```
   python manage.py runserver
   ```
   Access the site at `http://127.0.0.1:8000/`.

For production deployment, refer to Django's official docs on deploying with Heroku, AWS, or DigitalOcean.

## Usage

- **Admin Access**: Go to `/admin/` and log in with your superuser credentials to manage content.
- **Customize Content**: Edit models in `models.py` or add fixtures for sample data (e.g., `python manage.py loaddata fixtures/initial_data.json`).
- **Adding Games/News**: Use the admin panel to upload images and create entries.
- **Testing**: Run unit tests with `python manage.py test`.
- **Demo**: A live demo can be hosted on [Heroku](https://your-app.herokuapp.com) (deploy and link it here).

## Code Structure

```
Django-Project-1/
├── manage.py
├── requirements.txt
├── game_company/          # Main project folder
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── games/                 # App for game catalog
│   ├── migrations/
│   ├── templates/games/
│   ├── __init__.py
│   ├── admin.py
│   ├── models.py         # Game models
│   ├── views.py
│   ├── urls.py
│   └── forms.py
├── news/                  # App for blog/news
│   ├── ... (similar structure)
├── static/                # CSS, JS, images
├── templates/             # Base HTML templates
├── media/                 # Uploaded files (games screenshots)
└── .gitignore
```

- Apps are modular: `games` handles catalog, `news` manages blog.
- Templates use inheritance (base.html) for consistency.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a Pull Request.

Please follow PEP 8 style guidelines and include tests for new features. Issues and feature requests can be submitted via GitHub Issues.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by Django tutorials from official docs and Real Python.
- Thanks to Bootstrap for responsive components.
- Shoutout to the open-source community for libraries like CKEditor.
