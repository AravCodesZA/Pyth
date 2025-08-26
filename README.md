# ☁️ AWS Lambda & Image Processing 🖼️

This project implements an **AWS Lambda function** in Python for **facial image encoding**. This function is designed to support **mobile biometric authentication** workflows by converting facial images into a biometric template.

---

## ✨ Features

* **Facial Image Encoding:** Converts images into biometric templates for efficient processing.
* **Serverless Environment:** Optimized for deployment on **AWS Lambda**, ensuring a lightweight and scalable solution.
* **Mobile Integration:** Easily integrates into mobile authentication pipelines.
* **Minimal Dependencies:** Designed to be lightweight, with only essential libraries.

---

## 🛠️ Tech Stack

* **Python 3.x** 🐍
* **AWS Lambda**
* **AWS SDK (`boto3`)**
* **Image processing and encoding libraries** (e.g., `Pillow`, `face_recognition`)

---

## 📂 Project Structure

```

networkx/  (core algorithms and utilities)
tests/     (unit tests for validation)
utils/     (support functions)

````

> **Note:** The folder structure is optimized for packaging into AWS Lambda layers or zipped deployments.

---

## 🚀 Setup & Deployment

### 1. Install Dependencies

Install project dependencies into a local directory for packaging:

```bash
pip install -r requirements.txt -t ./package
````

### 2\. Package for Lambda

Navigate to the package directory, create a zip file, and then add the main function file to the archive:

```bash
cd package
zip -r ../lambda_function.zip .
cd ..
zip -g lambda_function.zip lambda_function.py
```

### 3\. Deploy to AWS

Upload the generated `lambda_function.zip` file to your AWS Lambda service. In the AWS Management Console, configure the handler to point to the main function.

```
lambda_function.lambda_handler
```

### 4\. Testing

You can invoke the deployed Lambda function with a sample event containing a Base64-encoded image string:

```json
{
  "image": "base64-encoded-image-string"
}
```

-----

## ✅ Use Cases

  * **Mobile Biometric Authentication**
  * **Secure User Identity Verification**
  * **Serverless, On-Demand Image Processing**

<!-- end list -->

```
```
