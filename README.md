# Text-to-SQL-with-Azure-OpenAI-and-Azure-SQL-Database
This project demonstrates how to use natural language to query an Azure SQL Database using Azure OpenAI's gpt-35-turbo-instruct model. The goal is to empower users to interact with a relational database using plain English, translating those queries into SQL and returning the results—all without needing to write a single line of SQL themselves.

### 🚀 Overview
In this solution:

We use AdventureWorks sample data hosted on an Azure SQL Database.

We leverage Azure OpenAI (GPT-35 Turbo Instruct model) for generating SQL queries.

We integrate everything in Jupyter Notebooks with the help of tools like LangChain, SQLAlchemy, and Azure OpenAI SDK.

Code is developed and tested in Visual Studio Code.

### 🧰 Tools & Technologies Used
Tool/Tech	Purpose
Azure SQL Database	Hosted relational data (AdventureWorks)
Azure OpenAI	Used GPT-35 Turbo Instruct for NL-to-SQL generation
LangChain	Chain LLM prompts with SQL execution logic
SQLAlchemy	ORM and database connection
azure-openai	Azure-hosted LLM integration
Python (Jupyter Notebooks)	Development and testing environment
VS Code	IDE for writing and testing code

###🔧 Setup Process
Create an Azure SQL Database

Populate it with AdventureWorks data.

Ensure firewall and connection settings are configured for remote access.

Create and Deploy Azure OpenAI Model

Use gpt-35-turbo-instruct.

Deploy the model under Azure OpenAI Studio.

Retrieve the endpoint and API key.

Store Secrets in .env File

Add both the Azure SQL connection string and Azure OpenAI credentials in .env:

env
Copy
Edit
AZURE_OPENAI_API_KEY=your_key
AZURE_OPENAI_ENDPOINT=https://your-endpoint.openai.azure.com/
AZURE_OPENAI_DEPLOYMENT=gpt-35-turbo-instruct
SQL_SERVER=your_sql_server.database.windows.net
SQL_DATABASE=AdventureWorks
SQL_USERNAME=your_username
SQL_PASSWORD=your_password
Install Required Python Libraries

bash
Copy
Edit
pip install langchain openai azure-openai sqlalchemy python-dotenv
Initialize LangChain and SQL Connection in Jupyter

Import libraries

Load environment variables

Set up SQL engine and LangChain LLM chain

Run Text-to-SQL Queries

Use .run("your question in plain English") to get SQL-generated answers from the database.

Example:

python
Copy
Edit
db_chain.run("How many customers do we have?")
