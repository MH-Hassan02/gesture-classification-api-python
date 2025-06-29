# Gesture Classification API

A Flask-based REST API for real-time gesture classification using machine learning.

## Features

- Real-time gesture classification from landmark data
- Confidence threshold filtering
- CORS enabled for frontend integration
- Font serving for web applications

## API Endpoints

- `GET /` - Health check endpoint
- `POST /predict` - Gesture classification endpoint
- `GET /type-font/<filename>` - Serve font files

## Usage

### Prediction Endpoint

Send a POST request to `/predict` with landmark data:

```json
{
  "landmarks": [
    [x1, y1, z1],
    [x2, y2, z2],
    ...
  ]
}
```

Response:
```json
{
  "gesture": "gesture_name",
  "confidence": 0.95
}
```

## Local Development

1. Install dependencies:
   ```bash
   pip install -r backend/requirements.txt
   ```

2. Run the server:
   ```bash
   cd backend
   python server.py
   ```

The server will run on `http://localhost:5001`

## Deployment

This project is configured for deployment on Render. The `render.yaml` file contains the deployment configuration. 