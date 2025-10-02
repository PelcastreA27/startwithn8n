# n8n Workflow Automation

This repository contains an **n8n workflow** that integrates multiple services to automate daily tasks and communication.

## Features
- Connects with **Google Sheets** to manage and store data.  
- Sends emails via **Gmail**.  
- Performs **HTTP requests** to external APIs.  
- Uses **Telegram** to send messages to each registered user.  
- Creates tasks automatically in **Google Tasks**.  
- Includes a **daily trigger** that sends a report via email with all registered users.  

## Testing
Currently, the workflow is tested using **Postman** to send data.  
However, it can easily be adapted to work with forms or other applications as input sources.  

## Usage
1. Import the workflow JSON into your n8n instance.  
2. Configure credentials for Google, Telegram, and any required APIs.  
3. Trigger the workflow manually or let the scheduled trigger run automatically.  

## 🗂 Workflow Diagram

```mermaid
flowchart LR
    A[Trigger / Postman or Form Input] --> B[Google Sheets]
    B --> C[Gmail: Send Email to User]
    B --> D[Telegram: Send Message]
    B --> E[Google Tasks: Create Task]
    F[Daily Trigger] --> G[Gmail: Send Daily Report]

## Workflow Diagram 
{
    "nombre completo": "Pepe Garzilla",
    "edad": 34,
    "mail": "mperez@gmail.com",
    "cel": 241545,
    "empresa": "put a name"
}
