# Chatbot API

A Flask-based REST API that provides conversational AI capabilities using a T5 transformer model. This API can be deployed locally or on cloud platforms like Railway.

## Features

- Simple REST API interface
- Powered by T5 transformer model
- Configurable response generation parameters
- Easy to deploy and scale

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

## Local Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd chatbbot-api
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the application:
```bash
python app.py
```

The API will be available at `http://localhost:5000`

## API Endpoints

### POST /chat
Send a message to the chatbot and receive a response.

**Request:**
```json
{
    "message": "Your message here"
}
```

**Response:**
```json
{
    "response": "AI generated response"
}
```

### GET /
Health check endpoint that returns a simple message indicating the API is running.

## Deployment on Railway

1. Create a Railway account at [railway.app](https://railway.app)
2. Install Railway CLI:
```bash
npm i -g @railway/cli
```

3. Login to Railway:
```bash
railway login
```

4. Initialize Railway project:
```bash
railway init
```

5. Deploy to Railway:
```bash
railway up
```

## Environment Variables

No environment variables are required for basic operation. The model is loaded from the local `chatbot_model` directory.

## Model Configuration

The API uses a T5 transformer model with the following generation parameters:
- Temperature: 0.8
- Top-k: 50
- Top-p: 0.95
- Max length: 1000 tokens

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the GitHub repository. 