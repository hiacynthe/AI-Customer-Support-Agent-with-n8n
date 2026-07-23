# AI Customer Support Agent with n8n

![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-orange)
![OpenAI](https://img.shields.io/badge/OpenAI-AI%20Agent-green)

## Overview

This project demonstrates how to build an intelligent customer support agent using **n8n** and **OpenAI**.

The AI agent answers customer questions by combining information from multiple business data sources instead of relying solely on the language model. It retrieves customer information from a CSV file, order data from a REST API, and uses conversational memory to provide contextual and accurate responses.

This project illustrates how AI agents can automate customer support while accessing real business data from multiple systems.

---

## Business Problem

Customer support teams often need to search across multiple applications before answering customer requests.

This manual process increases response time and may lead to inconsistent answers.

This workflow demonstrates how an AI agent can automatically retrieve, combine, analyze, and present information from multiple sources, enabling faster and more reliable customer support.

---

## Solution

The AI Customer Support Agent:

- Understands customer questions using OpenAI.
- Maintains conversation context with memory.
- Retrieves customer information from a CSV database.
- Retrieves order information from an external REST API.
- Combines data from both sources when necessary.
- Performs calculations and reasoning.
- Returns clear, natural-language answers.

---

## Workflow Architecture

```text
                    Customer Question
                            │
                            ▼
                     AI Customer Agent
                            │
          ┌─────────────────┼─────────────────┐
          ▼                 ▼                 ▼
   OpenAI Chat Model   Simple Memory      AI Tools
                                                │
                         ┌──────────────────────┴──────────────────────┐
                         ▼                                             ▼

              Customer Database (CSV)                    Orders Service (REST API)

                         └──────────────────────┬──────────────────────┘
                                                ▼

                                         AI Response
```

---

## Features

- 🤖 AI-powered customer support
- 💬 Conversational memory
- 📄 Customer data lookup
- 🌐 REST API integration
- 📊 Multi-source data retrieval
- 🔎 Intelligent reasoning
- ➕ Automatic calculations
- ⚡ Fast and contextual responses

---

## Data Sources

### Customer Database (CSV)

The customer database contains information such as:

- Customer ID
- Country
- Email
- Customer Since
- Region
- Subregion

Example:

```json
{
  "customerID": 1,
  "customerCountry": "India",
  "customerEmail": "customer1@mail.in",
  "customerSince": "2026-12-09T23:00:00.000Z",
  "region": "Asia",
  "subregion": "Southern Asia"
}
```

---

### Orders Service (REST API)

The Orders API provides information including:

- Order ID
- Customer ID
- Assigned Employee
- Product Category
- Quantity
- Order Price
- Order Status
- Order Date

Example:

```json
{
  "orderID": 1,
  "customerID": 8,
  "employeeName": "Mario",
  "orderPrice": 150.32,
  "quantity": 3,
  "productCategory": "Electronics",
  "orderDate": "2026-08-15T09:30:00",
  "orderStatus": "processing"
}
```

---

## Example Questions

The AI agent can answer questions such as:

- What region is customer 10 in?
- Which country does customer 15 belong to?
- What is the email address of customer 7?
- How many orders does customer 3 have?
- Who is the employee assigned to order 5?
- What is the status of order 12?
- What is the total order value for all electronics orders?
- Which customer placed the highest number of orders?
- What is the average order value?
- List all customers from Europe.

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| n8n | Workflow automation |
| OpenAI | AI reasoning and natural language responses |
| AI Agent | Intelligent orchestration |
| Simple Memory | Conversation context |
| CSV | Customer database |
| HTTP Request | REST API integration |
| REST API | Order information |
| JSON | Structured data exchange |

---

## Workflow Logic

### Step 1 - Receive User Question

The workflow starts when a customer submits a question.

---

### Step 2 - AI Analysis

The AI Agent analyzes the request and determines which data source(s) are required.

---

### Step 3 - Data Retrieval

Depending on the request, the agent retrieves information from:

- Customer CSV database
- Orders REST API

or both.

---

### Step 4 - Data Processing

The agent combines the retrieved information, performs any required calculations or reasoning, and prepares a response.

---

### Step 5 - Response Generation

OpenAI generates a professional and natural language response for the customer.

---

## Skills Demonstrated

This project demonstrates practical experience with:

- AI Agents
- Prompt Engineering
- Tool Calling
- Workflow Automation
- REST API Integration
- Data Integration
- Conversational AI
- Customer Support Automation
- Business Process Automation
- Multi-source Data Retrieval

---

## Repository Structure

```text
n8n-ai-customer-support-agent/

│
├── workflow/
│   └── workflow.json
│
├── sample-data/
│   ├── customers.csv
│   └── orders.json
│
├── images/
│   ├── workflow-overview.png
│   ├── architecture.png
│   └── demo-chat.png
│
├── docs/
│   └── project-documentation.pdf
│
└── README.md
```

---

## Demo

A complete workflow demonstration is available here:

**YouTube:** *(Add your video link)*

---

## How to Import the Workflow

1. Install n8n.
2. Open your n8n instance.
3. Select **Import Workflow**.
4. Import `workflow/workflow.json`.
5. Configure:
   - OpenAI credentials
   - REST API endpoint
   - Customer CSV file
6. Execute the workflow and start chatting with the AI Customer Support Agent.

---

## Sample Data

The repository includes sample datasets for demonstration purposes.

- `customers.csv`
- `orders.json`

These datasets are fictional and do not contain real customer information.

---

## Future Improvements

Potential enhancements for this project include:

- CRM integration (Salesforce, HubSpot, Odoo)
- Vector database for Retrieval-Augmented Generation (RAG)
- Knowledge Base integration
- Multi-language support
- Authentication and authorization
- Ticket creation in helpdesk systems
- Sentiment analysis
- Human agent escalation
- Dashboard and analytics

---

## Author

**Hiacynthe Temgoua**

Salesforce Consultant | AI Automation Specialist | n8n Developer

### Areas of Expertise

- Salesforce CRM
- AI Agents
- n8n Automation
- REST API Integration
- Business Process Automation
- Data Integration
- Workflow Design
- CRM Automation

---

## License

This project is provided for educational and portfolio purposes.
