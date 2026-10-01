# Car Price Prediction — Render Deployment

## Deploy on Render

1. Push this entire project folder to a GitHub repository.
2. Open Render and choose **New → Web Service**.
3. Connect the GitHub repository.
4. Select the branch containing this project.
5. Use:
   - **Runtime:** Python
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `gunicorn app:app`
6. Click **Create Web Service**.
7. Wait for the build and deployment to finish.
8. Open the public `onrender.com` URL.

## Important

This project is a Flask application. Do not deploy the complete application with GitHub Pages because GitHub Pages cannot run Python/Flask.

The model file and application files must remain in the repository. The Flask app should be started with:

`gunicorn app:app`

If your repository contains the Flask project inside a subfolder, set Render's **Root Directory** to that subfolder.

## Local test

Install dependencies:

`pip install -r requirements.txt`

Run:

`python app.py`

Then open the local address printed by Flask.
