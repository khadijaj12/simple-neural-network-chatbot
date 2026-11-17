# Simple Neural Network Chatbot

A chatbot that recognises the **intent** behind what you type (such as a greeting, a goodbye or a question) and replies with a matching response. A small neural network trained on a custom set of intents does the recognising.

## How it works

1. **Intents:** a dictionary of intents, each with example phrases (patterns) and possible replies.
2. **Preprocessing:** sentences are lowercased, stripped of punctuation, tokenised and stemmed with NLTK's Porter stemmer.
3. **Bag of words:** each sentence becomes a vector showing which known words it contains.
4. **Model:** a feed-forward neural network (Keras `Sequential` with `Dense` layers, trained with SGD) learns to map a bag of words to an intent.
5. **Chat loop:** the model predicts the intent of your message, and the bot replies with one of that intent's responses.

## Tech stack

Python · TensorFlow / Keras · NLTK · NumPy

## Running it

The script was written in Google Colab. To run it locally:

```bash
pip install -r requirements.txt
python chatbot.py
```

It trains the model first, then starts the chat. Type your messages at the `You:` prompt.

## Files

| File | Purpose |
|---|---|
| `chatbot.py` | Intents, preprocessing, model training and the chat loop |
| `requirements.txt` | Python packages needed |

## Author

Khadija Jawad, BS Artificial Intelligence, AWKUM
