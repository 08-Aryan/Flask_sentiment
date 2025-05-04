
# Flasking_the_sentiment

A simple, production-ready sentiment analysis API built with Flask. This project allows you to analyze the sentiment of text data using a pre-trained machine learning model, all wrapped in a lightweight and easy-to-deploy Flask application.

---

## 🚀 Features

- **RESTful API:** Easily analyze sentiment via HTTP requests.
- **Pre-trained Model:** Uses a serialized sentiment model for fast predictions.
- **Docker Support:** Includes a `Dockerfile` for containerized deployment.
- **Easy Setup:** Minimal dependencies, quick start with `requirements.txt`.

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/ZaRobot10/Flasking_the_sentiment.git
cd Flasking_the_sentiment
```

### 2. (Recommended) Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🏃‍♂️ Running the App

### Locally

```bash
python app.py
```

The API will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

### With Docker

```bash
docker build -t flasking_the_sentiment .
docker run -p 5000:5000 flasking_the_sentiment
```

---

## 📡 API Usage

### Endpoint

- **POST** `/predict`

### Request Body

```json
{
  "text": "Your text to analyze"
}
```

### Example (using `curl`)

```bash
curl -X POST http://127.0.0.1:5000/predict \
     -H "Content-Type: application/json" \
     -d '{"text": "I love using this app!"}'
```

### Example Response

```json
{
  "sentiment": "positive",
  "probability": 0.97
}
```

---

## 📁 Project Structure

```
Flasking_the_sentiment/
├── app.py                # Main Flask application
├── requirements.txt      # Python dependencies
├── Dockerfile            # For containerized deployment
├── sentiment_model.pkl   # Pre-trained sentiment analysis model
├── .gitignore
└── tempCodeRunnerFile.py # (Optional/temporary)
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to open an issue or submit a pull request.

---

*Happy Sentiment Analyzing!*
