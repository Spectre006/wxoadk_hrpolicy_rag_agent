# Watsonx Orcestrate HR Policy Agent using RAG
Agent which answers questions related with HR Policy using company's internal knowledge stored into RAG.

## RAG Connection Details
Create connection with Astra Vector DB on Cloud. Astra vector DB provides the ability to load data like PDFs directly. Below screne shots shows details of configuration performed :

![Create Astra DB database:](connection/AstraDB_Create_database.png)

![Load PDF using Data Explorer:](connection/AstraDB_Data_Explorer.png)

![Astra DB Connection added in WxO Knowledge:](connection/Knowledge_with_Agent.png)

![Knowledge Connection Details#1:](connection/AstraDB_Connection_1.png)

![Knowledge Connection Details#2:](connection/AstraDB_Connection_2.png)


## Add Cloud Environment:
``` 
orchestrate env add -n <environment-name> -u <service-instance-url> --type ibm_iam --activate 
```

## Activate Environment:
``` 
orchestrate env activate <<environment-name>>
``` 

## List all Environment Added:
``` 
orchestrate env list
``` 

## Import Agent:
``` 
orchestrate agents import -f /Users/prashantsharma/Documents/GitHub/wxoadk_hrpolicy_rag_agent/agents/hrpolicy_rag_agent.yaml
``` 

## List Agents:
``` 
orchestrate agents list
``` 