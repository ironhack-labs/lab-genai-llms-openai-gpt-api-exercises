![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | LLMs through an API


## Introduction

Over the last two days you routed a digital bank's customer messages with semantic search and with a fine-tuned DistilBERT, and both needed hundreds of labelled messages. In this lab you find out whether a large language model can do the same job with a good prompt and no training, and what it costs. Through the OpenAI API, you classify 60 real customer messages with zero-shot and few-shot prompts and compare the accuracy with yesterday's models, extract structured support tickets with Pydantic, draft replies that use the bank's policies and remember the conversation, and add up the cost of every step. In the extra task, the assistant checks a card's delivery status with function calling.

The lab follows the **LLMs through an API** lesson step by step.


## Getting Started

Open the `main.ipynb` file in the `your-code` directory. Follow the instructions, add your code, and answer the questions in the markdown cells. Each challenge ends with a checkpoint that tells you what you should see. The data is in the `data` folder: `messages.csv` has the 60 messages to classify and `examples.csv` 20 labelled examples for your prompts, both with the columns `text` and `category`.

The lab needs `pip install openai python-dotenv pydantic` and the OpenAI API key that Ironhack gives you. Create a file called `.env` in the `your-code` folder with one line, `OPENAI_API_KEY=sk-...`. The repository's `.gitignore` already excludes `.env`: **never write your key in the notebook, and run `git status` before every commit to check that `.env` is not listed.** The whole lab costs less than 5 US cents.

## Deliverables

- `main.ipynb` with your code, its outputs, and your answers.

## Submission

Upon completion, add your deliverables to git. Then commit git and push your branch to the remote.

## Resources

- [OpenAI API reference: Chat Completions](https://platform.openai.com/docs/api-reference/chat)
- [OpenAI guide: Structured outputs](https://platform.openai.com/docs/guides/structured-outputs)
- [OpenAI guide: Function calling](https://platform.openai.com/docs/guides/function-calling)
- [OpenAI pricing](https://platform.openai.com/docs/pricing)

## Data

The messages are a sample of the Banking77 dataset, created by PolyAI and published in [Efficient Intent Detection with Dual Sentence Encoders](https://arxiv.org/abs/2003.04807) (Casanueva et al., 2020). It is available at [PolyAI-LDN/task-specific-datasets](https://github.com/PolyAI-LDN/task-specific-datasets) under the [Creative Commons Attribution 4.0 licence](https://creativecommons.org/licenses/by/4.0/). `messages.csv` has 6 messages per intent from the original test set and `examples.csv` 2 per intent from the original training set, for ten of the 77 intents; the texts are unchanged.
