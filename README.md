# Create a Language Understanding Model with Azure AI Language Service

## Overview
In this lab, you will learn how to create a conversational language understanding model using Azure AI Language service. You will define intents, add sample utterances, train and test the model, and finally integrate it into a client application.

## Prerequisites

- Azure subscription
- Access to Azure portal
- Visual Studio Code installed
## Objectives
- Provision an Azure AI Language resource
- Create a conversational language understanding project
- Define intents and sample utterances
- Train and test the model
- Integrate the model into a Python client application

### 1. Provision an Azure AI Language Resource
- Sign in to the Azure portal using your Azure subscription credentials.
- Search for "Azure AI services" and select "Create" under Language Service.
- Configure the resource:
       - Subscription: 
       - Resource group: 
       - Region: 
       - Name:
       - Pricing tier: 
       - Responsible AI Notice:
       - Review and create the resource. Once deployed, navigate to the Keys and Endpoint page.
### 2. Create a Conversational Language Understanding Project
- Open the Azure AI Language Studio at Language Studio and sign in.
- Select your Azure AI Language resource.
- Create a new project:
- Name:
- Utterances primary language:
- Description:
Select "Create" to finalize the project.
### 3. Create Intents
On the Schema definition page, navigate to the Intents tab and add the intents:

### 4. Label Each Intent with Sample Utterances
........
Save your changes.
### 5. Train and Test the Model
- Start a training job for your model using standard training mode.
- After training succeeds, review the model performance metrics.
- Deploy the model and test it using various utterances to ensure it predicts intents correctly.
### 6. Add Entities
- Add a learned entityand label utterances.
- Add a list entity and specify valid values and synonyms.
- Add a prebuilt entity.
### 7. Retrain the Model
- After adding entities, retrain the model to incorporate the new schema.
- Deploy the updated model and test it with various utterances to ensure it recognizes intents and entities.
### 8. Use the Model from a Client App
Clone the provided GitHub repository: https://github.com/MicrosoftLearning/mslearn-ai-language.
Open the project in Visual Studio Code.
Install the Azure AI Language SDK for Python:
Open In Editor
`
pip install azure-ai-language-conversations
`
- Update the configuration file with your Azure Language resource's endpoint and key.
Implement the code to call the Language service model and handle user input.
- Run the application and test it with various utterances.
## Example
- Enter some text ("quit" to stop)
-- What time is it?
-- view top intent:
        - top intent: GetTime
        - category: GetTime
        - confidence score: 1

-- view entities:
-- query: What time is it?
-- 23:48

- Enter some text ("quit" to stop)
-- What's the date?
-- view top intent:
        -- top intent: GetDate
        -- category: GetDate
        -- confidence score: 0.9734405

-- view entities:
-- query: What's the date?
-- 11/10/2024

- Enter some text ("quit" to stop)
- quit
