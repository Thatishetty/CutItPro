# CutItPro - Link Shortening Service

**CutItPro** is an innovative Telegram bot designed to shorten and manage URLs, leveraging the power of AWS Serverless Services. This project combines the simplicity of Telegram Bot API with the scalability and efficiency of AWS Lambda and API Gateway, creating a seamless and reliable URL management solution.

---

## Key Features

- **Telegram Bot Integration**:  
  Interact with the bot through simple commands like `/start` and `/newbot`.  
  Real-time responses via Telegram BotFather API.

- **Serverless and Scalable Architecture**:  
  AWS Lambda for event-driven computation.  
  API Gateway for routing and REST API management.

- **Webhook Support**:  
  Securely integrates Telegram updates via webhook endpoints.

- **Cloud Monitoring**:  
  Tracks performance and logs events with AWS CloudWatch.

---

## Technologies Used

1. **Telegram Bot API**: For creating the bot interface and managing interactions.
2. **AWS API Gateway**: Handles routing of API requests and ensures scalability.
3. **AWS Lambda**: Processes backend logic for URL shortening and responses.
4. **AWS CloudWatch**: Provides logging and monitoring for troubleshooting and debugging.

---

## How It Works

1. **Telegram Commands**:  
   Users interact with the bot using commands:  
   - `/start`: Displays available services.  
   - `/newbot`: Initializes a new bot instance.

2. **API Gateway**:  
   Processes requests from Telegram’s webhook and routes them to Lambda.

3. **Lambda Functionality**:  
   Executes URL shortening and management logic.  
   Sends responses back to Telegram through the webhook.

4. **Webhook Integration**:  
   The bot uses a secure webhook endpoint hosted on API Gateway to receive updates from Telegram.

---

## Usage Instructions

### Prerequisites

- Telegram account.
- AWS account with API Gateway and Lambda access.
- Basic familiarity with serverless computing.

### Setup

1. **Register the Bot**:  
   - Use Telegram's BotFather to create a new bot.  
   - Obtain the HTTP token to interact with the Telegram API.

2. **Configure AWS Services**:  
   - Create an API Gateway endpoint to route incoming webhook calls.  
   - Deploy a Lambda function with the logic for URL shortening and user interaction.

3. **Webhook Integration**:  
   Use a tool like Postman or Curl to set up the webhook:

   ```bash
   POST https://api.telegram.org/bot<token>/setWebhook
   Body: {"url": "https://<your-api-endpoint>"}




   +---------------------+
|  Telegram User      |
+---------------------+
          |
          v
+---------------------+
|  Telegram Server    |
+---------------------+
          |
Webhook Integration
          |
          v
+---------------------+
|  AWS API Gateway    |
+---------------------+
          |
          v
+---------------------+
| AWS Lambda Function |
+---------------------+
          |
          v
+---------------------+
|  Response to User   |
+---------------------+

