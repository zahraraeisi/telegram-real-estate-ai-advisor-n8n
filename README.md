# Telegram Real Estate AI Advisor with n8n

A demo AI-powered real estate assistant built with **n8n**, **Telegram**, and **OpenAI**.

This workflow demonstrates how a real estate business can automate initial property inquiries, collect user requirements, match users with demo property listings, answer common questions, and capture leads in a structured conversation.

> This repository is a Demo / Proof of Concept. All project-specific names, credentials, IDs, private links, and sensitive information have been removed.

## What This Workflow Does

The assistant can:

- Collect property requirements in natural language
- Detect whether the user wants to rent or buy
- Detect city, budget, property type, and household size
- Ask follow-up questions when key information is missing
- Match users with the closest demo property listings
- Use AI to generate controlled property recommendations
- Answer common real-estate questions
- Collect advisor contact requests
- Collect property submission requests
- Store user session state in an n8n Data Table
- Continue conversations across multiple messages

## Example User Requests

Users can write requests such as:

- I need an apartment to rent in Berlin.
- I am looking for a student studio in Hamburg.
- I want to buy an apartment in Berlin for around €350,000.
- What is SCHUFA?
- What is Kaution?

## Example Flow

A typical property-search flow can look like this:

**Start → Smart Property Advisor → Requirement Detection → Follow-up Questions → Property Matching → AI Recommendation → Advisor Contact Request**

A lead-generation flow can look like:

**Start → Request Advisor Contact → Name → Phone → City → Budget → Notes → Confirmation**

## Main Features

### Smart Requirement Detection

The workflow can extract key information from natural-language messages, including:

- Rent or buy
- City
- Budget
- Property type
- Number of people

If required information is missing, the bot asks targeted follow-up questions.

### Property Matching

The public demo includes sample property listings.

The workflow scores listings against the user's requirements and returns the closest matching options.

### Controlled AI Recommendations

AI is used to turn structured property data into a more natural advisor-style response.

The AI is instructed not to invent:

- Properties
- Prices
- Availability
- Links
- Unsupported property details

### FAQ Handling

The workflow includes example FAQ topics such as:

- Rental documents
- SCHUFA
- Kaution
- Buying property as a foreign national

### Lead Collection

Users can submit:

- Advisor contact requests
- Property submission requests

The workflow collects structured information that can later be connected to a CRM, Google Sheets, or another lead-management system.

### Session Persistence

User session data is stored in an **n8n Data Table**, allowing the conversation flow to continue across multiple messages.

## Tech Stack

- n8n
- Telegram
- OpenAI
- JavaScript
- n8n Data Tables
- HTTP Requests

## Setup

After importing the workflow into n8n:

1. Create a Telegram bot.
2. Configure the Telegram Trigger credential.
3. Configure your OpenAI credential.
4. Create an n8n Data Table for session storage.
5. Replace `YOUR_DATA_TABLE_ID` with your Data Table ID.
6. Add the required Telegram bot token environment variable.
7. Test the full conversation flow before activating the workflow.

## Required Environment Variable

```env
TELEGRAM_BOT_TOKEN=YOUR_TELEGRAM_BOT_TOKEN
```

## Security

The public version of this workflow does not contain:

- Real Telegram bot tokens
- Real OpenAI credential IDs
- Private Data Table IDs
- Client names
- Project names
- Private property links
- n8n instance IDs
- Client-specific sensitive information

Never commit real credentials or private customer data to a public repository.

## Customization Ideas

This workflow can be adapted for:

- Real estate agencies
- Property marketplaces
- Rental platforms
- Relocation services
- Property lead qualification
- Property inquiry automation

It can also be extended with:

- CRM integration
- Google Sheets
- Website chat
- WhatsApp
- Property databases
- Real-time property availability
- Appointment booking
- Automated advisor assignment
- Multilingual support

## Disclaimer

This project is intended as a demonstration of AI-assisted real estate automation.

The included listings are sample data only.

The workflow does not provide definitive legal, tax, financial, immigration, or investment advice.

## Author

**Zahra Raeisi**

AI Automation Specialist

n8n • WordPress • WooCommerce • AI Agents • API Integrations
