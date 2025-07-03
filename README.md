# 🧠 Text-to-SQL with Azure OpenAI and Azure SQL Database

This project demonstrates how to use **natural language** to query an **Azure SQL Database** using **Azure OpenAI's `gpt-35-turbo-instruct`** model. The goal is to empower users to interact with relational data using plain English, automatically generating and executing the corresponding SQL behind the scenes.

---

## 🚀 Overview

- Uses **AdventureWorks** sample data hosted on **Azure SQL Database**  
- Leverages **Azure OpenAI (`gpt-35-turbo-instruct`)** to translate questions into SQL  
- Integration is done via **Jupyter Notebooks** using:
  - `LangChain`
  - `SQLAlchemy`
  - `azure-openai`  
- Development and testing is done in **Visual Studio Code**

---

## 🧰 Tools & Technologies Used

| Tool / Technology       | Purpose                                                |
|------------------------|--------------------------------------------------------|
| **Azure SQL Database** | Hosts the relational AdventureWorks data               |
| **Azure OpenAI**       | Converts natural language to SQL using GPT-35 Turbo    |
| **LangChain**          | Chains prompts and SQL execution                       |
| **SQLAlchemy**         | ORM and database connection                            |
| **azure-openai**       | SDK for connecting to Azure-hosted LLM                 |
| **Python / Jupyter**   | Development and testing environment                    |
| **Visual Studio Code** | IDE for building and testing the solution              |

---

## 🔧 Setup Instructions

### 1. Provision Azure SQL Database

- Create a new Azure SQL database
- Import the **AdventureWorks** sample data
- Configure firewall and access settings

### 2. Deploy GPT-35 Turbo on Azure OpenAI

- Use the `gpt-35-turbo-instruct` model (non-chat variant)
- Deploy via Azure OpenAI Studio
- Note down:
  - **Endpoint**
  - **Deployment name**
  - **API key**

### 3. Configure `.env` File

Create a `.env` file in your project root and include:

```env
AZURE_OPENAI_API_KEY=your_api_key
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_DEPLOYMENT=gpt-35-turbo-instruct

SQL_SERVER=your_sql_server.database.windows.net
SQL_DATABASE=AdventureWorks
SQL_USERNAME=your_username
SQL_PASSWORD=your_password
