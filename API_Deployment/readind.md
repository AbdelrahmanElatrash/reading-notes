# API Deployment

## What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?

- Keep settings in separate files: Split settings into multiple files based on their purpose (e.g., base settings, development settings, production settings) for better organization and maintainability.
- Use environment variables: Store sensitive information (e.g., secret keys, database credentials) in environment variables instead of hardcoding them in settings files.
- Utilize settings modules: Create separate Python modules to define and import settings, allowing for easy customization and overriding of default settings.
- Follow the "strict mode" principle: Raise an exception if any required settings are missing or misconfigured, ensuring that all necessary settings are properly defined.

## How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

- White Noise is a Python library that efficiently serves static files directly from Django applications during production.
- It serves static files without relying on a separate web server like Nginx or Apache, simplifying the deployment process.

### To integrate White Noise into a Django project:

- Install the White Noise library using pip.
- Add the whitenoise.middleware.WhiteNoiseMiddleware to the MIDDLEWARE setting in your Django project's settings file.
- Configure the static file handling in your settings file to use White Noise. This typically involves adding the STATICFILES_STORAGE setting and specifying the appropriate storage class provided by White Noise.
- Collect the static files using python manage.py collectstatic so that White Noise can serve them.

## What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?

CORS is a security mechanism that controls access to resources (e.g., APIs) on a different domain from the one serving the web page.
It prevents unauthorized cross-origin requests and ensures that only trusted origins can access resources.
In a Django project, CORS can be implemented using the django-cors-headers library.

### To configure CORS:

- Install the django-cors-headers library using pip.
- Add the corsheaders middleware to the MIDDLEWARE setting in your Django project's settings file.
- Configure the CORS_ALLOWED_ORIGINS setting to specify the list of trusted origins that are allowed to access the resources.
- Customize other CORS-related settings as needed, such as handling headers, methods, or credentials.