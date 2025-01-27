# django_oAuth

This project provides a Django-based web application with GitHub OAuth 2.0 authentication using the `django-allauth` library. It follows best practices for Django project setup, including a dedicated `setup` application, a `templates` directory for templates, and a Python virtual environment for development.

<div>

<img width="400" height="300" src="https://github.com/user-attachments/assets/ee74a48b-68e1-490d-85b3-f14f4aa9064f">
<img width="150" height="300" src="https://github.com/user-attachments/assets/527e6d16-037f-4397-98d3-5f2f23366bcf">
<img width="400" height="300" src="https://github.com/user-attachments/assets/65504250-48c7-4e91-9756-bb7b63443ba1">

</div>


## Key Features

*   **GitHub OAuth 2.0 Authentication:** Securely authenticate users using their GitHub accounts.
*   **Best Practices:** Follows Django project structure best practices, including:
    *   `setup` application for initial project configuration.
    *   `templates` directory at the project root for template organization.
    *   Python virtual environment for dependency management.
*   **Protected Member Area:** Utilizes Django's `@login_required` decorator to protect access to the member area.
*   **Two Main Views:**
    *   Homepage: Accessible to all users.
    *   Member Area: Requires authentication.

## Technologies Used

*   Python 
*   Django
*   django-allauth
*   OAuth 2.0

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   Python 3.x

### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Lucas-I-Marciano/django_oAuth.git
    ```

2.  Navigate to the project directory:

    ```bash
    cd django_oAuth
    ```

3.  Create a virtual environment (recommended):

    ```bash
    python3 -m venv venv  # On Linux/macOS
    python -m venv venv    # On Windows
    ```

4.  Activate the virtual environment:

    ```bash
    source venv/bin/activate   # On Linux/macOS
    venv\Scripts\activate.bat  # On Windows
    ```

5.  Install project dependencies:

    ```bash
    pip install -r requirements.txt
    ```

6.  Configure your GitHub OAuth application:

    *   Go to [https://github.com/settings/developers](https://github.com/settings/developers) and create a new OAuth App.
    *   Set the "Authorization callback URL" to `http://127.0.0.1:8000/accounts/github/login/callback/`.
    *   Copy the "Client ID" and "Client Secret".

7.  Create a `.env` file in the project's root directory and add the following, replacing with your actual values:

    ```
    SECRET_KEY=your_django_secret_key
    GITHUB_CLIENT_ID=your_github_client_id
    GITHUB_CLIENT_SECRET=your_github_client_secret
    ```

8.  Apply database migrations:

    ```bash
    python manage.py migrate
    ```

9.  Create a superuser (optional, but recommended for initial setup):

    ```bash
    python manage.py createsuperuser
    ```

10. Run the development server:

    ```bash
    python manage.py runserver
    ```

11. Access the application in your browser at `http://127.0.0.1:8000/`.

## Usage

*   Visit the homepage at `/`.
*   Access the member area at `/members/` (requires login).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

[Choose a License, e.g., MIT](LICENSE) (Adicione o arquivo de licença no seu repositório)
