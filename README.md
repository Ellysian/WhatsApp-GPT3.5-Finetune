# Project Overview

This project aims to finetune OpenAI's GPT3.5 chat model using WhatsApp chat messages. The goal is to emulate the messaging style of a specific user based on their previous conversations. To do this, we parse and segment the chat data based on timestamps, grouping messages into conversations based on the time gap between them. 

The project is structured around OpenAI's guide on fine-tuning, and we welcome any suggestions for improving the efficiency of this process.

## Installation

To install, you first need to clone the repository to your local machine. Open your terminal and run the following command:

```
git clone https://github.com/Ellysian/WhatsApp-GPT3.5-Finetune.git
```

After cloning the repository, navigate to the project directory:

```
cd WhatsApp-GPT3.5-Finetune
```

Then, you can install the necessary requirements by running:

```
pip install -r requirements.txt
```

Note: It is recommended to use a virtual environment to avoid conflicts with other projects.

## Data Preparation 

1. Export the WhatsApp chat you want to use for finetuning. On WhatsApp, open the desired chat, tap the three dots on the top right > More > Export chat > Without media. Unpack the archive and place the `_chat.txt` file in the project folder.

2. Follow the instructions in the `preprocessing.ipynb` file to preprocess the data. For Step 4, you can find the names in the `_chat.txt` file. For example:
```
[23.08.23, 12:47:15] John Doe: Apples
[23.08.23, 12:49:03] Jane Doe: Why the sky?
```
In this case, the names are "John Doe" and "Jane Doe".

## Fine-tuning

1. Set up your OpenAI API key in the `.env` file as follows: `OPENAI_API_KEY="your_api_key"`

2. Follow the instructions in the `fine-tuning.ipynb` file to fine-tune the model.

## Usage

Once the fine-tuning is complete, the trained model will be available on OpenAI's servers. You can interact with this model using the conventional API or via the OpenAI playground.
