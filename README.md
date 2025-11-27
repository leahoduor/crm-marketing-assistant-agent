<p align="center">
  <img src="https://raw.githubusercontent.com/leahoduor/crm-marketing-assistant-agent/main/Banner.png" width="100%" />
</p>
 **If you find this project helpful, please give the repository a star.It helps others discover it!**

# CRM/Marketing Assistant Agent
 
 
 **README.md — CRM/Marketing Assistant Agent**

\# CRM/Marketing Assistant Agent    
\#\#\# Multi-Agent Workflow for Lead Research, CRM Updates, Email Automation & Content Scheduling    
\*\*Kaggle x Google Agents Intensive – Capstone Project\*\*    
\*\*By: Leah Oduor “Leah The Digital VA\*\*.”

\---

\#\# Overview    
This project is a \*\*multi-agent AI system\*\* designed to automate common CRM and marketing tasks for small businesses and solopreneurs. It performs:

\- Lead research    
\- CRM updating    
\- Follow-up email generation    
\- Content scheduling  

The system is built as a \*\*4-agent sequential workflow\*\*, orchestrated by a central coordinator.    
This mirrors an enterprise pipeline and demonstrates core Agent Development Kit (ADK) concepts:    
tools, agents, context passing, observability, and model integration.

This repository contains:    
\- Full Kaggle notebook    
\- Architecture diagram    
\- Documentation of all agents    
\- Simulated tools for safe, reproducible execution

\---

\#\#  Problem Statement    
Small businesses struggle to manage CRM tasks effectively. Lead follow-ups, CRM updates, writing emails, and planning content require time they don’t have.    
This leads to:

\- Missed opportunities    
\- Slow client response times    
\- Poor marketing consistency    
\- Lost revenue  

This project automates these tasks using \*\*AI agents that work together.\*\*

\---

\#\#  Why Agents?    
The CRM workflow comprises \*\*multiple steps\*\* that require different actions, tools, and context.    
Agents are ideal because they:

\- Automate sequential multi-step pipelines    
\- Use specialized tools    
\- Maintain context between tasks    
\- Scale repetitive work    
\- Mirror real human roles (research → CRM → email → scheduling)

This system utilizes \*\*four specialized agents\*\*, each responsible for a specific business function.

\---

\#\#  Architecture  

\#\#\# \*\*System Diagram\*\*

               ┌──────────────────────────┐  
               │     User Input (Lead)    │  
               └─────────────┬────────────┘  
                             │  
                             ▼  
                ┌────────────────────────┐  
                │    Orchestrator Agent  │  
                └─────────────┬──────────┘  
                             │  
 ┌───────────────────────────┼──────────────────────────┐  
 ▼                           ▼                          ▼

┌───────────────┐ ┌────────────────┐ ┌─────────────────┐  
│ LeadResearch │ │ CRMUpdater │ │ EmailGenerator │  
│ Agent │ │ Agent │ │ Agent │  
└──────┬────────┘ └───────┬────────┘ └────────┬────────┘  
│ │ │  
▼ ▼ ▼  
Search Tool CRM API Tool Template/LLM Tool  
(SERPAPI simulated) (Airtable simulated) (Gemini simulated)

                             │  
                             ▼  
                 ┌────────────────────────┐  
                 │ ContentSchedulerAgent  │  
                 └─────────────┬──────────┘  
                               │  
                               ▼  
                    Social Scheduler Tool  
                       (Zapier simulated)

\#\#\# Agents    
| Agent | Role | Tools |  
|-------|-------|-------|  
| \*\*LeadResearchAgent\*\* | Fetches basic company info | Search Tool (SERPAPI simulated) |  
| \*\*CRMUpdaterAgent\*\* | Updates Airtable-like CRM | CRM API Tool (simulated) |  
| \*\*EmailGeneratorAgent\*\* | Generates personalized follow-up email | Gemini-style LLM (simulated) |  
| \*\*ContentSchedulerAgent\*\* | Schedules marketing posts | Scheduler Webhook Tool (simulated) |  
| \*\*Orchestrator\*\* | Coordinates all agents | Executes pipeline sequentially |

\---

\#\#  Tech Stack    
\- \*\*Python\*\*    
\- \*\*Multi-Agent Architecture\*\*    
\- \*\*Search, CRM, and Scheduler Tools\*\* (simulated for Kaggle safety)    
\- \*\*Gemini-compatible Email Generator\*\*    
\- \*\*Kaggle Notebook for development\*\*    
\- \*\*GitHub for version control\*\*  

This design is deployment-ready for:

\- \*\*Vertex AI Agent Engine\*\*    
\- \*\*Google Cloud Run\*\*    
\- \*\*FastAPI microservice\*\*  

\---

\#\# Features    
✔ End-to-end automated workflow    
✔ Modular agent design    
✔ Safe simulated API tools    
✔ Clear separation between agents and tools    
✔ Simple orchestrator pipeline    
✔ Ready for real-world API integration    
✔ Perfect for portfolio, client demos, or expansion into SaaS

\---

\#\#  Notebook    
The Kaggle Notebook contains:

\- Full implementation of the 4 agents    
\- Tool definitions (simulated)    
\- Orchestrator pipeline    
\- Demo execution (\`run\_full\_pipeline("Acme Corp")\`)    
\- Documentation & Markdown  

\---

\#\# Demo Output Example    
When running:

\`\`\`python  
run\_full\_pipeline("Acme Corp")

The system returns:

Lead profile

CRM update status

Generated follow-up email

Scheduled post status

All without any manual input.

     **ADK Concepts Demonstrated**

This project fulfills the ADK-based agent design used in the Kaggle x Google Intensive:

Multi-agent system design

Tool-based interactions

Context passing

Sequential orchestration

Model-driven generation (Gemini simulated)

Observability through logs & fallbacks

    **Future Improvements**

With more time, the system could include:

Real Gemini Pro integration

Live SERPAPI, Airtable, Zapier connections

Long-term memory for lead history

Web UI dashboard (Next.js or Streamlit)

Deployment on Cloud Run / Agent Engine

A2A protocol for deeper agent collaboration

Analytics and reporting engine

 Author

Leah Oduor ”Leah The Digital VA”  
