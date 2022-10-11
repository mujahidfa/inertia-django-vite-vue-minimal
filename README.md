# Inertia + Django + Vite + Vue minimal template

A minimal, working template for Inertia + Django + Vite + Vue.

## Technologies

1. Inertia - powered by the official [Inertia.js Django Adapter](https://github.com/inertiajs/inertia-django)
2. Django v4.1
3. Vite 3 - powered by [Django Vite](https://github.com/MrBin99/django-vite)
4. Vue 3
5. TypeScript
6. [WhiteNoise](https://whitenoise.evans.io/en/stable/index.html) - to serve static files

## How to install & run

1. Download the repo. You can either:

   a. Clone the repo (without the git history):

   ```sh
   npx degit https://github.com/mujahidfa/inertia-django-vite-vue-minimal
   ```

   b. Or, create a repo based on this template via the [GitHub template generator](https://github.com/mujahidfa/inertia-django-vite-vue-minimal/generate).

2. Install required Python packages.

   ```sh
   # Create and activate a virtual environment
   python3 -m venv .venv
   source .venv/bin/activate

   # Install required Python packages
   pip install -r requirements.txt
   ```

3. Install required Node.js packages.

   ```sh
   npm install
   ```

4. Run the Vite dev server:

   ```sh
   npm run dev
   ```

5. Run Django's default migrations:

   ```sh
   python manage.py migrate
   ```

6. Run the Django dev server (in a separate terminal):

   ```sh
   python manage.py runserver
   ```

## How to build for production

1. Set `DEBUG=False` in [settings.py](./inertia_django_vite_vue_minimal/settings.py).

   ```py
   # In settings.py
   ...
   DEBUG=False
   ...
   ```

2. Build the JS/assets for production:

   ```sh
   npm run build
   ```

3. Run `collectstatic`:

   ```sh
   rm -rf staticfiles/
   python manage.py collectstatic
   ```

4. Run the Django server:

   ```sh
   python manage.py runserver
   ```
