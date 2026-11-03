# Real-World Applications and Project Ideas

## Real-World Applications

Prompt engineering makes AI applications more efficient and effective. Application developers typically wrap open-ended user input inside a prompt before passing it to the model.

Consider an AI chatbot. A user might enter an incomplete request like "Where to purchase a shirt." Internally, the application uses an engineered prompt such as: "You are a sales assistant for a clothing company. A user, based in Alabama, United States, is asking where to purchase a shirt. Respond with the three nearest store locations that currently stock a shirt." The chatbot then returns more relevant and accurate information. (See [AWS Prompt Engineering](https://aws.amazon.com/what-is/prompt-engineering/).)

These techniques are actively used in production by major companies worldwide.

**From [LangGraph in Production](https://www.langchain.com/blog/is-langgraph-used-in-production):**

- **Klarna**: an AI customer support assistant serving 85 million active users, reducing customer resolution time by 80%.
- **LinkedIn**: an AI-powered recruiter that automates candidate sourcing, plus an SQL bot that turns natural language questions into SQL queries.
- **Uber**: automated unit test generation for large-scale code migrations using multi-agent systems.
- **AppFolio**: an AI copilot saving property managers 10+ hours per week, with a 2x improvement in decision accuracy.

**From [Top LangGraph Agents in Production 2024](https://www.langchain.com/blog/top-5-langgraph-agents-in-production-2024):**

- **Cisco Outshift**: an AI Platform Engineer that boosts developer productivity 10x, reducing CI/CD pipeline setup from one week to under one hour.

**From [LangChain Use Cases (Airbyte)](https://airbyte.com/data-engineering-resources/langchain-use-cases):**

- Organisations report that LangChain pipelines shorten deployment by 3-5x and reduce manual data engineering tasks by up to 80%.
- LangChain is used by 100,000+ companies worldwide for document Q&A, conversational AI, and automated knowledge systems.

## Taking It Further: Project Ideas

After completing the workshop you have the skills to build your own prompt engineering applications. Here are two projects that apply what you have learned.

### 1. Job Application Assistant

Analyse job postings and extract structured information (skills, requirements, experience levels).

Workflow:

1. Paste the job posting text.
2. Extract requirements with a prompt template.
3. Categorise skills using few-shot examples.
4. Generate a cover letter outline through a chained prompt.

Extensions: compare multiple postings, generate tailored resume bullets, create a skills gap analysis.

### 2. Content Transformation Pipeline

Convert content between formats (for example technical docs to beginner guides, or meeting notes to action items).

Workflow:

1. Start with the source content.
2. Use few-shot examples for the desired transformation.
3. Build a chain: `extraction_prompt | llm | formatting_prompt | llm | output_parser`.
4. Batch process multiple documents.

Examples: meeting notes to action items, research papers to summaries, code docs to tutorials.

## Getting Started

Pick a project that solves a real problem you have, and start simple:

1. Define your input and desired output clearly.
2. Create a basic prompt template with the four components (instruction, context, input variable, output indicator).
3. Test with a few examples manually.
4. Add few-shot examples if the formatting is complex.
5. Build chains if you need multi-step processing.
6. Scale with batch processing.
