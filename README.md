# Automate-Event-Planning


Event Planning Automation with CrewAI
A Python-based automated event planning system using CrewAI that coordinates venue booking, logistics management, and marketing activities through AI agents.
Overview
This project uses CrewAI to create three specialized AI agents that work together to plan and execute events:

Venue Coordinator: Finds and books appropriate venues
Logistics Manager: Handles catering and equipment arrangements
Marketing and Communications Agent: Promotes the event and engages attendees

Prerequisites

Python 3.7+
OpenAI API key
Serper API key (for web search capabilities)

Installation
Install the required packages:
bashpip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
Configuration
Set up your API keys using the utility functions:
pythonfrom utils import get_openai_api_key, get_serper_api_key

openai_api_key = get_openai_api_key()
os.environ["SERPER_API_KEY"] = get_serper_api_key()
Usage

Define your event details:

pythonevent_details = {
    'event_topic': "Tech Innovation Conference",
    'event_city': "San Francisco",
    'tentative_date': "2024-09-15",
    'expected_participants': 500,
    'budget': 20000,
    'venue_type': "Conference Hall"
}

Run the crew:

pythonresult = event_management_crew.kickoff(inputs=event_details)
Output Files
The system generates two output files:

venue_details.json: Contains venue information (name, address, capacity, booking status)
marketing_report.md: Marketing activities report in Markdown format

Features

Automated venue search and booking
Logistics coordination (catering, equipment)
Marketing campaign management
Human-in-the-loop validation for critical decisions
Asynchronous task execution for improved performance
Structured output in JSON and Markdown formats

