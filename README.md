
# Browser_Use – Automated AI Product Reviewer

This project is a small AI agent that automatically browses **Product Hunt**, collects information about the top products of the day, and generates short reviews using a language model.
The reviews can also be converted into speech using a text-to-speech system.

The goal of the project was to experiment with **AI agents that combine browser automation, LLM reasoning, and voice output** in a single workflow.

---

## What it does

The script runs an automated flow:

1. Opens Product Hunt using **Playwright**
2. Finds the top products of the day
3. Extracts basic information (name, description, link)
4. Sends that information to an **LLM API**
5. Generates a short review
6. Converts the review into **speech using TTS**

At the end, the program produces:

* A **text review**
* An **audio narration** of the review

---

## Tech Stack

* **Python 3**
* **Playwright** – browser automation
* **LLM API** – for generating product reviews
* **TTS (Text-to-Speech)** – converts the review to audio
* **Browser-Use framework** – for agent workflow

---

## Project Workflow

```
Product Hunt Page
       ↓
Playwright Scraping
       ↓
Extract product details
       ↓
Send data to LLM
       ↓
Generate review
       ↓
Convert review to speech
       ↓
Save / display output
```

---

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/itsDurvank/Browser_Use.git
cd Browser_Use
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure environment variables

Copy the example file:

```bash
cp .env.example .env
```

Add your API key inside `.env`.

### 4. Install Playwright browsers

```bash
playwright install
```

### 5. Run the script

```bash
python main.py
```

---

## Example Output

Example generated review:

```
Product X is a productivity tool designed to simplify task management.
The interface is clean and focuses on reducing friction when organizing daily work...
```

The same review is also generated as an **audio narration** using text-to-speech.

---

## Why I built this

I wanted to explore how **AI agents can combine multiple capabilities**:

* browser automation
* LLM reasoning
* speech generation

into one workflow.

This project is mainly an experiment in **agentic automation using real web data**.

---
