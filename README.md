# AI-Powered Voice Travel Agent | n8n Automation

An end-to-end, voice-first travel-planning workflow built with **n8n**, **ElevenLabs Titan Voice Agent**, **Tavily**, **SerpAPI**, and **OpenAI**. The workflow collects a traveller’s preferences through a voice conversation, researches relevant travel options, generates a personalized itinerary, and emails the final plan to the traveller.

## ✨ Features

- **Voice-first intake:** Collects trip details through a conversational AI voice agent.
- **Confirmation before processing:** Confirms the collected information with the traveller before continuing.
- **Personalized destination research:** Uses Tavily to discover activities that match the traveller’s interests.
- **Flight and accommodation search:** Uses SerpAPI to find relevant flight and resort options.
- **AI-generated itinerary:** Uses an OpenAI model to organize the research into a clear, tailored travel plan.
- **Automated email delivery:** Sends the formatted itinerary to the traveller’s email address.

## 🔄 Workflow

1. **Collect traveller details** through the ElevenLabs Titan Voice Agent.
2. **Confirm the details** before starting the research workflow.
3. **Research destination activities** with Tavily, based on the traveller’s preferences.
4. **Search flights and resorts** with SerpAPI.
5. **Generate the travel plan** using an OpenAI model, combining the collected details and search results.
6. **Format and send the email** containing the personalized plan.

## 🧳 Information Collected

The voice agent asks the traveller for:

- Number of travellers
- Origin
- Destination
- Departure date
- Arrival/return date
- Preferred activities at the destination
- Email address

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| [n8n](https://n8n.io/) | Workflow orchestration and automation |
| [ElevenLabs](https://elevenlabs.io/) Titan Voice Agent | Conversational voice-based data collection |
| [Tavily](https://tavily.com/) API | Destination and activity research |
| [SerpAPI](https://serpapi.com/) | Flight and resort search |
| [OpenAI](https://openai.com/) | AI-powered itinerary creation and email formatting |

## 🧠 Personalization

The itinerary is tailored to the traveller’s stated interests, which may include:

- Adventure and outdoor activities
- Relaxation and resort experiences
- Cultural and sightseeing experiences
- Nightlife
- Food and local experiences

The AI organizes the available research into a readable plan. Search results and availability may change, so travellers should verify prices, schedules, and booking details before making reservations.

## ⚙️ Setup

This repository describes the workflow. To run it, you will need accounts and API credentials for the services used.

1. Set up an n8n instance.
2. Configure the ElevenLabs voice agent to collect the required trip details and confirm them with the traveller.
3. Connect the voice agent to the n8n workflow using your chosen integration method.
4. Add credentials for Tavily, SerpAPI, and OpenAI in n8n.
5. Configure the workflow nodes to pass the confirmed trip details to the research and itinerary-generation steps.
6. Configure an email node or email provider to send the final itinerary.
7. Test the workflow with sample trip details before using it for real travel plans.

> **Note:** Exact node names, connection methods, and configuration depend on your n8n workflow and service setup. Add your exported n8n workflow JSON to this repository if you want others to import and run the automation.

## 🔐 Environment Variables & Credentials

Store API keys and email credentials securely using **n8n Credentials** or your deployment’s secret-management system. Do not commit API keys, access tokens, passwords, or personal traveller information to version control.

Typical credentials required:

- ElevenLabs API / agent configuration
- Tavily API key
- SerpAPI key
- OpenAI API key
- Email provider credentials

## 📁 Suggested Repository Structure

```text
.
├── README.md
├── workflows/
│   └── voice-travel-agent.json   # Exported n8n workflow (add this file)
└── .gitignore
```

Example `.gitignore` entries:

```gitignore
.env
.env.*
!.env.example
```

## ✅ Example Output

The traveller receives a personalized email containing a structured travel plan, which can include:

- Trip summary
- Flight options found through search
- Resort or accommodation options
- Recommended activities
- A day-by-day itinerary, where sufficient information is available
- Relevant links and practical notes

The exact contents depend on the search results and the workflow configuration.

## 🚧 Limitations

- Search results may be incomplete, outdated, or unavailable.
- Prices, flight schedules, accommodation availability, and activity details can change.
- The workflow provides research and recommendations; it does **not** automatically book flights or accommodation unless a separate booking integration is added.
- Review the generated itinerary and verify all details before booking.

## 🔮 Possible Enhancements

- Add budget and travel-class preferences.
- Include weather and local transportation information.
- Add multi-destination trip support.
- Generate a PDF itinerary alongside the email.
- Add follow-up questions when required details are missing.
- Integrate booking providers, with explicit user confirmation before purchases.
- Add error handling, retries, and workflow execution alerts.

## 👤 Author

Created as an AI automation project using n8n and connected AI/search services.

---

**If you find this project useful, feel free to ⭐ the repository!**
