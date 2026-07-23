# AI-Customer-Support-Agent-with-n8n
AI-powered customer support agent built with n8n. Uses OpenAI, conversational memory, customer data from CSV, and order information from a REST API to answer customer questions, retrieve records, perform calculations, and provide accurate business insights automatically.

Overview

This project demonstrates how to build an intelligent customer support agent using n8n and OpenAI.

The AI agent answers customer questions by combining information from multiple business data sources instead of relying solely on the language model.

The solution integrates customer records stored in a CSV file with order information retrieved from an external REST API, enabling the agent to provide accurate and contextual responses.

Business Problem

Customer support teams often need to access information stored across multiple systems before answering a customer's request.

Switching between applications increases response time and reduces productivity.

This workflow demonstrates how an AI agent can automatically retrieve, combine and analyze information from multiple sources to provide instant answers.

Solution

The AI agent:

Understands customer questions
Chooses the appropriate data source
Retrieves the required information
Performs calculations when necessary
Generates a natural language response
Workflow Architecture
                User Question
                      │
                      ▼

                 AI Agent
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼

 OpenAI Chat     Simple Memory   AI Tools
                                     │
                     ┌───────────────┴───────────────┐
                     ▼                               ▼

            Customer Database               Orders API
              (CSV File)                   (REST API)

                     │
                     └───────────────┬───────────────┘
                                     ▼

                              AI Response
Features
AI-powered customer service
OpenAI integration
Conversation memory
Customer lookup
Order lookup
Multi-source data retrieval
Automatic reasoning
Dynamic calculations
Natural language responses
Data Sources
Customer Database (CSV)

Contains:

Customer ID
Country
Region
Subregion
Email
Customer Since
Orders API

Contains:

Order ID
Customer ID
Assigned Employee
Product Category
Quantity
Order Price
Order Status
Order Date
Example Questions

The AI agent can answer questions such as:

What region is customer 10 in?
How many orders does customer 3 have?
Who is the employee assigned to order 5?
What is the total value of all electronics orders?
Which customer placed the most orders?
What is the status of order 12?
Which customers belong to Europe?
What is the average order value?
Technologies
n8n
OpenAI
AI Agent
Simple Memory
CSV
HTTP Request
REST API
Skills Demonstrated

This project demonstrates practical experience in:

AI Agents
Prompt Engineering
Tool Calling
Workflow Automation
REST API Integration
Data Integration
Conversational AI
Customer Support Automation
Repository Structure
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
Demo

A complete demonstration is available here:

(Add your YouTube link)

Import

Import the workflow into n8n and configure:

OpenAI credentials
HTTP endpoint
Customer CSV location
Author

Hiacynthe Temgoua

Salesforce Consultant | AI Automation | n8n Developer

Ce qui rend ce projet encore plus fort

Par rapport à ton premier workflow, celui-ci montre des compétences très recherchées en 2026 :

IA générative avec OpenAI ;
AI Agent avec mémoire conversationnelle ;
Tool Calling (l'agent choisit les bons outils) ;
Intégration de données (CSV + API REST) ;
Raisonnement et calculs à partir de données métier.

En plaçant ce projet juste après ton Multi-Source Sales Reporting Pipeline, ton portfolio montrera une progression logique : d'abord l'automatisation et l'intégration de données, puis la création d'un agent IA capable d'exploiter ces données pour répondre à des demandes métier. C'est une combinaison très convaincante pour des clients ou des recruteurs.
