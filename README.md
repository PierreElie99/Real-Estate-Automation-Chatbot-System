# Real Estate Automation Chatbot (n8n)

**Overview:**  
This is a fully automated real estate chatbot built using **n8n**. It handles property inquiries, collects client details, manages appointment scheduling, and assists with human agent handoffs. The system intelligently processes user messages, extracts relevant information, searches properties from the database, and confirms appointments via email and Google Calendar.

**Key Features:**  
- **Smart Information Extraction:** Automatically extracts personal details (name, phone, email) and property requirements (type, location, budget, timeline, citizenship) from user messages.  
- **Content Filtering:** Ensures that only property-related queries are handled; gracefully ends unrelated conversations.  
- **Human Agent Handoff:** Collects necessary information before forwarding requests to a human agent via email.  
- **Property Search Automation:** Queries a PostgreSQL database to provide the most relevant property listings based on user criteria.  
- **Appointment Management:** Automates scheduling, confirmation, and calendar updates using Gmail and Google Calendar.  
- **Conversational AI:** Uses OpenAI models within n8n for natural, professional responses.  
- **Sequential Data Collection:** Only asks for missing information, avoiding repeated questions.  

**Technologies & Tools Used:**  
- **n8n:** Workflow automation and orchestration  
- **PostgreSQL:** Property and user information storage  
- **Google Calendar & Gmail:** Appointment scheduling and notifications  
- **OpenAI GPT-4 & GPT-4o-mini:** Natural language understanding and conversational responses  
- **SerpAPI (optional):** Property search enrichment  

**Workflow Overview:**  
1. **Webhook Trigger:** Receives user messages.  
2. **Data Parsing:** Extracts links, personal info, and property requirements.  
3. **Content Filtering:** Checks if the request is relevant to real estate.  
4. **Human Agent Check:** For requests to contact a human agent, collects necessary info and sends email.  
5. **Property Search:** Queries the database to find matching properties.  
6. **AI Formatting:** Formats search results into friendly, readable responses.  
7. **Appointment Handling:** Collects preferred dates, checks availability, schedules in Google Calendar, and sends confirmation emails.  

**Benefits:**  
- Reduces manual workload for real estate agents.  
- Provides fast, accurate, and professional responses to customer inquiries.  
- Streamlines appointment scheduling and follow-ups.  
- Ensures consistency in client communication.  

**Repository Structure:**  

**Usage Instructions:**  
1. Import `workflow.json` into n8n.  
2. Configure PostgreSQL, Google Calendar, Gmail, and OpenAI credentials.  
3. Activate the workflow.  
4. Users can now interact with the chatbot via the webhook endpoint.  

**Author:**  
Pierre Ellie  
[GitHub Profile](https://github.com/PierreElie99)

