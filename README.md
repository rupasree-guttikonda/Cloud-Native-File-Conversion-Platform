# Cloud-Native File Conversion Platform

A serverless file conversion platform built on AWS that enables users to upload PDF, PNG, and JPEG files and convert them into different formats through a web-based interface and REST APIs.

## Overview

This project leverages AWS serverless services to provide a scalable and cost-effective file conversion solution. Users can upload files through a frontend application or API endpoint, and the system automatically processes the conversion using AWS Lambda before securely storing the output in Amazon S3.

## Features

* Convert PDF to PNG
* Convert PDF to JPEG
* Convert PNG to JPEG
* Convert JPEG to PNG
* Secure file storage using Amazon S3
* REST API integration via API Gateway
* Automated processing using AWS Lambda
* Download converted files using pre-signed URLs
* Serverless architecture with minimal infrastructure management

## Architecture

User → API Gateway → AWS Lambda → Amazon S3 (Input Bucket)

AWS Lambda → File Conversion Logic → Amazon S3 (Output Bucket)

User ← Pre-Signed Download URL ← AWS Lambda

## Tech Stack

### Cloud Services

* AWS Lambda
* Amazon S3
* API Gateway
* IAM

### Backend

* Python
* Boto3

### File Processing

* PyMuPDF
* Pillow (PIL)

### Frontend

* HTML
* JavaScript
* REST APIs

## Supported Conversions

| Source Format | Target Format |
| ------------- | ------------- |
| PDF           | PNG           |
| PDF           | JPEG          |
| PNG           | JPEG          |
| JPEG          | PNG           |

## Project Workflow

1. User uploads a file through the web interface.
2. API Gateway receives the request.
3. Lambda validates the file and conversion type.
4. Source file is stored in the input S3 bucket.
5. Lambda performs the conversion using PyMuPDF or Pillow.
6. Converted file is stored in the output S3 bucket.
7. A pre-signed URL is generated for secure download.
8. User downloads the converted file.

## Key Learning Outcomes

* Designing serverless architectures on AWS
* Building REST APIs with API Gateway
* Implementing file processing workflows using Lambda
* Managing secure storage with Amazon S3
* Configuring IAM roles and permissions
* Integrating frontend applications with cloud services
* Working with Python libraries for document and image processing

## Future Enhancements

* Support DOCX to PDF conversion
* Multi-page PDF processing
* Batch file conversion
* User authentication using Amazon Cognito
* CloudWatch monitoring and logging
* Docker-based Lambda deployment
* Additional file format support

## Contributors

* Rupa Sree Guttikonda – Lambda Development, File Conversion Logic
* Sathwika Cherukuri – AWS Infrastructure, S3, API Gateway, IAM Configuration

## Author

Rupa Sree Guttikonda

MS Computer Science | Software Engineer | Cloud & Full Stack Development Enthusiast
