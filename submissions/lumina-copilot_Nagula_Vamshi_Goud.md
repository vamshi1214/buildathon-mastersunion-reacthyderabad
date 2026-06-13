# Project Submission Template

# Project Name

lumina-copilot

## Attendee Details

**Name:** Nagula Vamshi Goud
**GitHub Username:** vamshi1214
**LinkedIn Profile:** https://www.linkedin.com/in/nagula-vamshi-goud-6026ab217
**GitHub Project Repository:** Your project repository link

---

## Problem Statement Selected

```txt
HR Cost Intelligence Engine
```


## Project Description


## Approach

What is the project about?
The project is a specialized operational intelligence dashboard designed to convert calendar events, meeting schedules, and employee hours into real-time health and cost-allocation insights. Centered on a tailored HR Manager (Wellbeing) view, it quantifies how much time employees spend collaborating versus working independently.

Who is it for?
It is primarily built for HR Managers, People Operations staff, and Team Leaders who are responsible for monitoring organizational health, optimizing productivity, and protecting teams from meeting overload.

What problem does it solve?
Unstructured calendar schedules and excessive meetings create two major problems:
Employee Burnout: Team members buried under endless meetings lose their valuable "deep focus" working hours, leading to fatigue, overtime, and severe burnout.
Invisible Financial Waste: Organizations often have no clear idea what their meetings actually cost. This system calculates the direct financial footprint (e.g., Total Meeting Cost and Average Meeting Cost) based on the salaries of the attendees involved.

How does it help the user?
Burnout Radar: Automatically flags team members who spend more than 40% of their business hours in meetings (representing high meeting overhead), allowing HR to protect their quiet focus time.
Cost Quantification: Breaks down meeting expenditures by department and project, turning vague calendar data into clear cost metrics.
Actionable Advice: The Lumina smart recommendation engine provides concrete, wellness-focused policy suggestions (such as establishing company-wide post-6 PM "Calendar Quiet Hours" or moving daily status standups to asynchronous text updates).
Clear Metrics: Visualizes trends in "wasted hours" and "wasted focus blocks" to help leadership back up workspace policies with real, easy-to-understand data.

## Tech Stack and Tools Used
Frontend:
Framework: React 19 (Functional Hooks and Context APIs structured under a single-screen design focusing on dashboard density)
Build System: Vite 6 (High-speed module bundling)
Styling & Design: Tailwind CSS v4 (Using raw utility classes, custom spacing rhythms, and high-contrast styling)
Animations: Motion (motion/react for micro-animations and staggered visual entries)
Data Visualizations: Recharts (Dynamic bar charts, cost trend graphs, and interactive hover gauges)
Iconography: Lucide React
Backend:
Runtime: Node.js
Framework: Express (RESTful custom proxy endpoints for handling data retrieval, updates, and secure AI requests)
Bundler & TS Execution: tsx (TypeScript dev runner) & esbuild (Fast CommonJS compilation of the custom server entry point)
Database:
Database: Local JSON Database with server-side read/write operations for meeting tracking, user overrides, and cost-center allocations.
AI Tools/API:
API SDK: Gemini API via @google/genai (For real-time meeting categorization, keyword attribution, and confidence scoring)
Other Tools:
Workspace Engine: Google AI Studio Build Command Workspace
Linter: TypeScript (tsc --noEmit) for clean static check validation

## Key Features

AI-Powered Schedule & Project Attribution
Utilizes server-side Gemini models to analyze meeting topics, agendas, and attendee rosters to automatically assign events to specific development project codes with detailed reasoning and classification confidence scores.
Burnout & Meeting Load Analytics (Wellbeing Focus)
Calculates the precise percentage of business hours employees spend inside live meetings, automatically flagging individuals facing extreme meeting saturation (exceeding 40% of their working hours) to mitigate burnout risks and support HR wellbeing initiatives.
Intelligent Cost Leakage & Wastage Auditing
Dynamically scans past and recurring meetings for structural waste markers—such as large audience fatigue (over 8 active attendees) or redundant frequency patterns—quantifying financial leakage and generating mitigation strategies (e.g., "Two-Pizza criteria").
Interactive Lumina Copilot Chatbot
Integrates an interactive chat assistant backed by server-side Gemini intelligence, enabling HR managers to query corporate meeting datasets for immediate visual trend reviews, cost-driver insights, and structural policy recommendations.
Live Financial Calibration & External Integrations
Provides real-time CRUD and wage rate updates on employee profiles, triggering immediate global recalculations of average meeting costs and financial data points, along with a custom interface to run external Google Calendar synchronizations.

## What is Working?

The application is completely compiled, linted, and fully functional:
The Entire Cost & Revenue Calculation Engine: Recalculates cost estimates, total meeting durations, and wasted focus hours live as employee salaries are edited.
Database Synchronization: Synchronized backend endpoints (/api/costs, /api/meetings, /api/employees, and custom update methods) fetch information without losing client state.
Advanced Filters: Real-time project-level selection and Gemini Confidence levels (Low vs. High confidence event classifications) can be filtered interactively.
Interactive Modals: The dialog options to override AI project attributions and custom-sync raw calendar imports are fully functional.


## What is Still in Progress?

Active Outlook/GSuite Connectors: Integrating direct OAuth API links to fetch calendars directly from Microsoft Graph or Google Workspace, rather than relying entirely on seeded organizational structures.

## Screenshots or Demo

Add screenshots, demo video link, or deployed project link if available.

**Deployed Link:**
**Demo Video Link:**
**Screenshots:**<img width="1900" height="835" alt="image" src="https://github.com/user-attachments/assets/23f843b4-145e-4e98-a9c7-24c4be0516e9" />
<img width="1896" height="803" alt="image" src="https://github.com/user-attachments/assets/8a5a0aec-bd38-4459-a6f5-a723550a8fa9" />



---

## Challenges Faced

Correlating Multi-Attendee Overhead: Simulating true corporate schedules without generating overlapping scheduling conflicts took precise matrix seeding to ensure employees weren't booked into two meetings at the exact same hour.
Minimizing Render Cascades: Live cost recalculations across 500+ meetings and 50 employees on slider adjustments required caching metrics to maintain instant UI response rates.

## Learnings

The Scale of Meetings: Standard corporate administrative syncs are incredibly expensive when fully computed. A simple 30-minute status meeting with senior leads easily costs thousands of Rupees. Exposing this hard data is a massive eye-opener for managers.
Tailwind Engineering: Leveraging modern CSS and pure utility-first designs creates highly accessible, readable layouts without cluttering the client-side codebase.

## Future Improvements

Anonymization Modalities: Adding secure client-side filters to mask individual base salaries with average band rates to comply with strict privacy policies when presenting to the wider company.
Pre-Meeting Budget Calculators: Build a Google Calendar extension that shows organizers the estimated cumulative cost of a meeting before they click "Send invite".

## Final Note

Use this space to add anything else you want mentors, judges, or the community to know about your project.

Write your answer here.
