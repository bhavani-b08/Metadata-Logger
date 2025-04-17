# 📁 AWS Lambda S3 Metadata Logger

This project is a **serverless AWS Lambda function** that automatically captures and logs metadata of files uploaded to an **S3 bucket** and stores it in a **DynamoDB** table.

## 📌 Features

- Triggered by S3 file upload event
- Extracts file metadata:
  - Bucket Name
  - File Name (Object Key)
  - File Size
  - File Type
- Stores metadata in DynamoDB with a unique ID

## ⚙️ Tech Stack

- AWS Lambda (Python)
- Amazon S3
- DynamoDB
- Boto3 (AWS SDK for Python)

## 🧠 How It Works

1. A file is uploaded to the specified S3 bucket.
2. Lambda function is automatically triggered by an S3 event.
3. Metadata is fetched using `head_object`.
4. Data is stored in a DynamoDB table (`mtadata`).
