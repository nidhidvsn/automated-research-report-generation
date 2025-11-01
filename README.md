Here's an explanation of the project flow which appears to be an autonomous research report generation system:

Core Components
1. Report Generation Workflow
The main workflow is handled by AutonomousReportGenerator class which coordinates these key steps:

Create Analysts: Generates AI analyst personas based on the research topic
Human Feedback: Allows human input to refine analyst selection
Conduct Interviews: Runs parallel interview workflows with each analyst
Write Report: Compiles sections into a unified report
Finalize Report: Adds introduction, conclusion and formats the final document
2. Interview Workflow
The InterviewGraphBuilder handles the interview process:

Generate questions
Perform web search using Tavily
Generate expert answers
Save interview transcript
Write report section
3. State Management
The project uses several state classes to manage workflow:

GenerateAnalystsState: Manages analyst creation
InterviewState: Handles interview flow
ResearchGraphState: Maintains overall report state
4. API Layer
The ReportService provides API endpoints:

Flow Sequence
User submits topic through API
System generates analyst personas
Optional human feedback loop
Parallel interview processes run
Sections compiled into report
Report formatted and saved as PDF/DOCX
User can download final report
The project uses LangGraph for workflow orchestration and includes comprehensive logging and error handling through CustomLogger and ResearchAnalystException.

---

Autonomous Research Report Generator
An AI-powered system that generates comprehensive research reports by coordinating multiple AI analyst personas, conducting interviews, and synthesizing findings.

🌟 Features
Generates diverse AI analyst personas based on research topics
Conducts parallel interview workflows with each analyst
Performs web searches using Tavily API
Compiles findings into structured reports
Exports reports in both PDF and DOCX formats
Provides interactive human feedback loop
🚀 Getting Started
Prerequisites
Python 3.8+
Poetry (for dependency management)
Required API keys:
OpenAI API key
Google AI API key
Groq API key
Tavily API key
Installation
Configuration
Create a .env file in the project root:
Update config.yaml if needed (located in research_and_analyst/config/)
💻 Usage
Running the Web Interface
Visit http://localhost:8000 in your browser

Using as a Python Package
📁 Project Structure
🤝 Contributing
Fork the repository
Create your feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
LangGraph for workflow orchestration
LangChain for LLM interactions
Tavily for web search capabilities
FastAPI for web interface
For more detailed documentation, please refer to the docs/ directory.