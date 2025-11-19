# takneev5

takneev5 is a web application designed for artists to showcase and sell their artwork. It provides a platform for artists to manage their portfolio, connect with a community of fellow artists, and reach a wider audience. The application also leverages AI to provide features like price suggestions, artwork description generation, and content moderation.

## Features

- **Artist Portfolio:** Artists can create a profile, upload their artwork, and manage their portfolio.
- **Marketplace:** A marketplace where users can browse and purchase artwork from various artists.
- **Community Hub:** A space for artists to share posts, interact with each other, and build a community.
- **AI-Powered Tools:**
    - **Price Suggestion:** Get AI-powered price suggestions for your artwork based on images and details.
    - **Description Generation:** Automatically generate compelling descriptions for your artwork.
    - **Content Moderation:** AI-powered validation to filter out inappropriate content in reviews and messages.
- **QR Code Generation:** Generate QR codes for artist profiles and artwork pages for easy sharing.
- **User Authentication:** Secure user authentication system for artists and users.
- **Contact Form:** A contact form for users to get in touch with the platform administrators.

## Tech Stack

- **Backend:** Python, Flask
- **Database:** MySQL
- **AI:** Google Generative AI (Gemini)
- **Frontend:** HTML, CSS, JavaScript
- **Libraries:**
    - `Flask`
    - `mysql-connector-python`
    - `google-generativeai`
    - `Pillow`
    - `qrcode`
    - `colorama`

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/takneev5.git
    cd takneev5
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up the database:**
    - Make sure you have a MySQL server running.
    - Create a database named `takneev5`.
    - Create a copy of `config/config.ini.example` and rename it to `config/config.ini`.
    - Update the `config/config.ini` file with your database credentials and your Google Generative AI API key.
      ```ini
      [DATABASE]
      host = localhost
      user = your_db_user
      password = your_db_password
      database = takneev5

      [API]
      gemini_api_key = your_gemini_api_key
      ```

5.  **Run the application:**
    ```bash
    python app.py
    ```
    The application will be running at `http://localhost:7777`.

## Project Structure

```
takneev5/
├── .gitignore
├── app.py                  # Main Flask application file
├── requirements.txt        # Python dependencies
├── brain/                  # Contains AI-related logic
│   ├── ai_image_enhancer.py
│   ├── config.py
│   ├── db_setup.py
│   ├── description_generator.py
│   ├── message_validator.py
│   ├── price_generator.py
│   └── review_validator.py
├── config/
│   └── config.ini          # Configuration file for database and API keys
├── static/                 # Static assets (CSS, JS, images)
│   ├── css/
│   ├── js/
│   ├── assets/
│   ├── product-images/
│   └── uploads/
└── templates/              # HTML templates
    ├── about.html
    ├── artist_arts.html
    ├── community.html
    ├── contact.html
    ├── feedback_popup.html
    ├── index.html
    ├── join.html
    ├── layout.html
    ├── marketplace.html
    ├── product_detail.html
    ├── studio.html
    └── tools.html
```
