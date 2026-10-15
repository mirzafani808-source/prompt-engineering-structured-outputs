# Prompt Engineering & Structured Outputs — Support Ticket Triage

Turns raw customer support tickets into **validated JSON** using an LLM (Groq free tier, Llama 3.3 70B).

## Features
- Bad prompt vs improved prompt comparison on the same input
- JSON schema enforced with Pydantic (`category`, `priority`, `sentiment`, `summary`, `action_items`, `needs_human`)
- Few-shot examples + consistency test (5 runs, same input)
- Safe parsing: strip code fences, validate schema, retry with error feedback
- Context window manager: token estimate, summarize old turns, hard-trim fallback
- Batch evaluation: % valid outputs, bad vs improved prompt

## Run
1. Get a free key: https://console.groq.com/keys
2. Open `prompt_engineering_structured_outputs.ipynb` in Google Colab
3. Colab sidebar -> Secrets (key icon) -> add `GROQ_API_KEY`, enable notebook access
4. Runtime -> Run all

## Stack
Python, Groq API, Pydantic, Google Colab
