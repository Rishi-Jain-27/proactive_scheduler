# proactive_scheduler

# Project Title

Final project for the Building AI course by the University of Helsinki.

## Summary
Echo is a conversational AI that parses unstructured chat messages into precise, time-sensitive remidners. It removes the friction of manual data entry acting instead as an assistant that you can tell exactly what you need to remember and it remains

## Background
Managing a high-density schedule feels like a second job. The transition from hearing a deadline to actually recording it is where most tasks fall through the cracks.
* Problem one is calendar friction. Manual entry into apps like Google Calendar is tedious and often skipped.
* Problem two is information fragmentation. Critical details are scattered across emails, group chats, and verbal announcements.
* Problem three is cognitive load. The mental overhead of remembering to check a planner reduces the focus for actual work.
I wanted to build a system that moves at the speed of thought. Instead of a static grid of boxes, I wanted an assistant that listens to my life and intervenes when necessary.

## How is it used?
Echo is used through a simple chat interface (web or mobile). Whenever a user encounters a piece of information they need to remember, they simply dump it into the chat.
The user inputs nay information.
Echo identifies the intent, the subject, location, and time, as well as any other necessary information.
Echo briefly acknowledges, and then at the designated time, Echo sends a push notification or message to ensure the user is where they need to be.

## Data sources and AI methods
| Source/Method      | Description                                             |
| ------------------ | ------------------------------------------------------- |
| User Input         | Real-time text or voice transcripts provided by the user|
| LLM                | Used for Named Entity Recognition to extract dates, times, and task intent from messy text.|
| Vector Database    | A retrieval-augmented generation setup to remember past context (e.g., knowing who "the coach" is)|
| Temporal Logic     | Python-based scheduling libraries (like APScheduler) to trigger events based on LLM output|

## Challenges
Echo is a memory assistant, so it has specific limitations.
* Hallucinations. LLMs can misinterpret wording or hallucinate a time if the input is too vague.
* Privacy. Since the system processes personal schedules, ensuring data is encrupted and not used for external training is a major ethical hurdle.
* Task execution. Echo reminds you, but cannot make you do the work or prioritize your tasks.

## What next?
The next phase is proactive intelligence. Instead of waiting for a reminder, Echo could look at a syllabus or a series of deadlines and suggest things to the user. To get there, I would need to sync school portals with mail clients using an API, and I would need advanced prompt engineering to reduce temporal reasoning errors in the LLM.

## Acknowledgments
* This was inspired by the "Building a Second Brain" by Tiago Forte.
* The technical foundations are built using the OpenAI API and Python open-source libraries.
* Course guidance was provided by the University of Helsinki.
