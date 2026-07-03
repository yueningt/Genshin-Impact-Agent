# Genshin-Impact-Agent
Agent that can answer questions regarding characters, lore, and other information about Genshin Impact game. 

## 1. Data Acquisition
The dataset is generated via a custom headless browser scraper built on **Playwright**. The scraper is engineered to fully extract comprehensive wiki page content—including dynamic tabs, collapsed sections, and virtualized story panels—aggregating into a structured local text corpus (~30.5 MB).

## 2. Gemini-Powered Analysis Engine
The `genshin_wiki_agent_gemini.ipynb` notebook implements the analytical pipeline leveraging Google's **Gemini 2.5 Flash** model. This notebook connects securely via the official API to run fast, cost-efficient text evaluation and multi-turn reasoning workflows.

## 3. DeepSeek Analysis Suite
The repository offers two execution tracks for leveraging DeepSeek's reasoning models:

* **Cloud Deployment (`genshin_wiki_agent_deepseek_api.ipynb`):** Connects directly to the cloud-hosted DeepSeek API for accelerated inference.
* **Local Deployment (`genshin_wiki_agent_deepseek.ipynb`):** Executes locally without an external network connection or API keys. This pipeline utilizes the distilled [DeepSeek-R1-Distill-Llama-8B](https://huggingface.co) model hosted on Hugging Face.
