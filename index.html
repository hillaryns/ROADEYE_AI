from flask import Flask, request, jsonify
from flask_cors import CORS
import requests
import os

app = Flask(__name__)
CORS(app)

ROBOFLOW_API_KEY = os.environ.get("ROBOFLOW_API_KEY")

MODEL = "pothole-detection-i00zy-dwqjk/1"

@app.route("/detect", methods=["POST"])
def detect():
    try:
        image_base64 = request.json["image"]

        url = f"https://detect.roboflow.com/{MODEL}"

        response = requests.post(
            url,
            params={
                "api_key": ROBOFLOW_API_KEY,
                "confidence": 30
            },
            data=image_base64,
            headers={
                "Content-Type": "application/x-www-form-urlencoded"
            }
        )

        return jsonify(response.json()), response.status_code

    except Exception as e:
        return jsonify({"error": str(e)}), 500


if __name__ == "__main__":
    app.run(port=5000, debug=True)
