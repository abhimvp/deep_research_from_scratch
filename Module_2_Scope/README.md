# Notes from module 2 : Scope

You'll learn to implement the first major element of our deep research agent, which is `Scoping`.

This is a process of going for an open-ended conversation with the user to gather context about the request to a research brief that can be taken by our agent and used to ground & steer the entire research process.

This just has two simple steps:

- First is, conversing with user in gathering context about their request.
- Second is, just generating a research brief -> which describes what the aim of research should be.
- Also learn to set up and run evaluations

--> this is very good practice because as we build out our agent , we're going to run evaluations on each sub-component in isolation.

- this let's us test our system as we build it out to make sure each piece is working as expected.

---

Notebook Reference: `1_scoping.ipynb`

Get API Keys of following and add them into `.env`:

- [TAVILY API KEY](https://app.tavily.com/home)
- [Google API Key](https://aistudio.google.com/app/apikey)
- [LangSmith API Key](https://smith.langchain.com/)

We can run Jupyter Notebooks directly:

```bash
uv run jupyter notebook
# or
# activate venv and just do
jupyter notebook
# it opens up the notebooks in browser.
```

---

Adding [ChatGoogleGenerativeAI](https://python.langchain.com/docs/integrations/chat/google_generative_ai/) instead of using default init_chat_model as it doesn't give access to general gemini models.

- go-through in detail of code and evaluations in langsmith to get better understanding

---

1. User Clarification and Brief Generation (notebooks/1_scoping.ipynb)

Purpose: Clarify research scope and transform user input into structured research briefs

Key Concepts:

User Clarification: Determines if additional context is needed from the user using structured output
Brief Generation: Transforms conversations into detailed research questions
LangGraph Commands: Using Command system for flow control and state updates
Structured Output: Pydantic schemas for reliable decision making

Implementation Highlights:

Two-step workflow: clarification → brief generation
Structured output models (ClarifyWithUser, ResearchQuestion) to prevent hallucination
Conditional routing based on clarification needs
Date-aware prompts for context-sensitive research

---

What You'll Learn: State management, structured output patterns, conditional routing
