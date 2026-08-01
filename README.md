# ECG Arrhythmia Diagnosis Platform

This Django project combines **ECG deep learning arrhythmia classification** with an **interactive 3D heart visualization**.

## Quick start

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt

python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Then open `http://127.0.0.1:8000/` in your browser.

## Features

- User registration and login (`accounts` app)
- Dashboard with links to analysis and visualization
- ECG upload and arrhythmia prediction (`ecg_analysis` app)
- 3D heart / AR-style visualization (`visualization` app)

## Model file

Place your trained Keras model at:

```text
ecg_analysis/ml_model/arrhythmia_model.h5
```

The `predict.py` module expects a softmax output and defines a few example class labels you can adjust.

