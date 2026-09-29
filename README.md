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
