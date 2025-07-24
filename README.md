### Voice AI Agent for Restaurants

Automating customer service through intelligent voice technology, powered by ElevenLabs, n8n, and Google Sheets

## 📌 Introduction
In a fast-paced hospitality industry, restaurants often struggle with managing customer reservations, handling inquiries, and providing real-time updates—all without overwhelming staff. This project introduces a Voice AI Agent that automates these repetitive tasks through lifelike voice interaction, seamlessly combining smart workflow automation, data-driven decisions, and natural speech synthesis.

## Tools

n8n:  Visual automation engine managing all logic, API calls, conditionals, and tool orchestration.
Google Sheets: Live database for reservation details, orders, customer info, and dynamic responses.
ElevenLabs: Speech generation platform converting text into rich, humanlike voice replies.
Custom Tools: Modules for detecting language, retrieving specific rows from Sheets, formatting text, and routing queries.

## Workflow Summary:
User input → Detect intent & language →
→ Lookup data in Google Sheets →
→ Format response →
→ Convert response to speech via ElevenLabs →
→ Return voice output

## Benefit

Hands-free Customer Support: Eliminates manual answering of common queries with fluent, expressive voice replies.
- 📈 Real-time Accuracy: Pulls live data from Sheets, ensuring information is always up to date.
- 🕒 Saves Staff Time: Reduces human workload for routine tasks like checking bookings or confirming menu details.
- 🌍 Multilingual Support: Adapts voice responses to customer language supports regional communication effortlessly.
- 🔄 Scalable & Modular: Add new features like payment queries, feedback collection, or chatbot handoffs without rewriting core logic.
- 

## Problems

1. Overwhelmed Front Desk or Customer Service Teams  
   Restaurants often receive repetitive calls and messages asking about reservations, orders, or operating hours, leading to staff burnout.

2. Manual Reservation Confirmations  
   Staff must manually check spreadsheets, confirm bookings, and respond to customers, causing delays and errors.

3. No Voice Automation for Real-Time Data  
   Most voice bots cannot dynamically pull reservation or order data stored in platforms like Google Sheets.

4. Limited Language or Accessibility Support  
   Traditional restaurant bots offer limited multi-language voice interaction, which excludes regional or non-English-speaking customers.

5. Scalability Challenges for Multi-Branch Restaurants  
   Expanding support to multiple locations requires rebuilding workflows and retraining staff—adding cost and complexity.

6. Lack of Emotional Engagement  
   Text-based bots feel cold and robotic; customers prefer a warm, friendly human-like interaction.

## ✅ Solutions

1. Automated Voice Response System  
   Using ElevenLabs, the agent speaks fluently and emotionally confirming reservations, orders, and menu info without staff intervention.

2. Google Sheets Integration for Real-Time Data Access  
   The n8n workflow reads live booking or order information directly from Sheets and converts it into accurate spoken replies.

3. Multilingual Voice Support  
   The built-in language detection module switches the response to the customer’s preferred language automatically.

4. Modular Workflow via n8n  
   Each restaurant branch can clone the same flow, link it to its own Sheets, and activate voice service without extra coding.

5. Emotion-Rich Speech for Better UX  
   ElevenLabs allows for voice customization, friendly, formal, enthusiastic—making customer interaction feel personalized.

6. Scalable, Low-Code Automation  
   Thanks to n8n, this project is extendable, low-code, and cost-effective to maintain and deploy.

  ### Data File

   
## 📄 Menu Data Extraction Workflow  
### PDF-to-Text Conversion for Dynamic Voice Responses

This workflow enables the Voice AI Agent to dynamically respond to customer menu queries by extracting text from a stored PDF file. It is designed to be **triggered by another workflow**(i.e Voice AI Agent Workflow), making it modular and reusable across different automation flows.

### 🔧 Workflow Components

| Node                        | Description                                              |
|-----------------------------|----------------------------------------------------------|
| **Execute Workflow Trigger**| Activated by another workflow to begin extraction        |
| **Download PDF File**       | Retrieves the menu PDF from Google drive     |
| **Extract Text from PDF**   | Converts content into plain text for AI voice responses  |

### 🧠 Problem Solved

- ❌ Static, hardcoded menus limit flexibility and create update overhead  
- ❌ Manual entry of menu items is time-consuming and error-prone  
- ❌ Voice agent can’t access current menu data in real time

### ✅ Solution Provided

- ✅ Automatically parses the menu from the PDF file  
- ✅ Modular: triggered by other workflows whenever menu is needed  
- ✅ Sends extracted text to ElevenLabs or chatbot for natural voice delivery

### 📦 Use Case Example

> **Customer says:** “What’s available for lunch?”  
> ✅ Voice AI triggers the extraction workflow  
> ✅ PDF is downloaded and parsed  
> ✅ Text extracted: _“Grilled Chicken ₦3,000, Jollof Rice ₦2,500...”
> ✅ ElevenLabs speaks it back clearly and naturally
