# AI-Powered Issue Reporting & Sentiment Aggregator Agent

An autonomous AI agent designed to ingest, categorize, prioritize, and summarize public service issues reported by citizens. It automatically routes urban complaints to relevant municipal departments while providing real-time sentiment and severity analytics.

---

## Target Audience
* **City Administrators & Municipal Staff:** To quickly view prioritized issue queues, route tickets, and monitor citizen sentiment trends.
* **Citizens:** To submit structured or unstructured issue reports and receive automated classification and status updates.

---

## Quick Start & Reproduction Guide

Follow these steps to set up and run the agent locally on Linux/macOS or Windows.

### Prerequisites
* Python 3.10+
* Git
* An active API key for OpenAI, Anthropic, or Google Gemini

### 1. Clone the Repository
bash
git clone [https://github.com/nomanamir20/smartcity-ai-agent.git](https://github.com/nomanamir20/smartcity-ai-agent.git)
cd smartcity-ai-agent

### 2. Set Up Virtual Environment

# Windows
python -m venv venv
venv\Scripts\activate

###3. Install Dependencies

pip install -r requirements.txt

###4. Configure Environment Variables

Create a .env file in the root directory and add your credentials:

API_KEY=your_actual_api_key_here
LOG_LEVEL=INFO
ENVIRONMENT=development

###5. Run the Agent

python main.py

###Usage Examples
Example 1: Terminal Ingestion & Direct Output
Run the agent in interactive terminal mode:

python main.py --input "There is a severe water leak near Main Market, block B causing traffic congestion."

###Agent Output:

{
  "category": "Infrastructure / Water Supply",
  "priority_score": 0.88,
  "urgency": "High",
  "assigned_department": "Water & Sanitation Authority",
  "sentiment": "Frustrated / Urgent",
  "summary": "Severe water leak causing traffic blockage near Main Market Block B."
}


###System Architecture:

                                  +-----------------------+
                                  | Citizen Issue Input   |
                                  +-----------+-----------+
                                              |
                                              v
                                  +-----------------------+
                                  | Preprocessing & Token |
                                  | Normalization         |
                                  +-----------+-----------+
                                              |
                                              v
+------------------------+        +-----------------------+
| Knowledge / Context    | <----> | Autonomous AI Agent   |
| Database               |        | Reasoning Engine      |
+------------------------+        +-----------+-----------+
                                              |
                                              v
                                  +-----------------------+
                                  | Guardrails & Priority |
                                  | Scoring Evaluation    |
                                  +-----------+-----------+
                                              |
                                              v
                                  +-----------------------+
                                  | Structured Output /   |
                                  | Department Dispatch   |
                                  +-----------------------+



###Known Limitations:

1. Language Constraint: Currently optimized primarily for English inputs. Urdu or mixed Roman-Urdu queries may experience higher categorization error rates.

2. Context Window Limits: Issues containing excessively long descriptions (>2,000 tokens) are automatically truncated, which may omit minor secondary details.

3. No Real-Time API Hook: Department routing currently outputs structured JSON; direct API payload posting to municipal software requires manual endpoint binding.
