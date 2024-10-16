# Project Title: Face Your Emotions (Grow with Google, Google Machine Learning Program)

## Project Overview

Often, people want others to feel the strongest emotion they are experiencing, even when they aren't sure what that core emotion is. "Face Your Emotions" helps detect and amplify this core emotion, creating responses that reflect the user’s emotional state.

The model operates in two steps:

First, we fine-tuned two models (BERT and Gemma 2 2B) to detect emotions accurately.

Secondly, we created a second model using Gemma 2 2B it using Unsloth and LoRA techniques to generate emotionally resonant responses each aligned with six distinct emotional characters.

Through carefully designed prompts and fine-tuning hyperparameters, the model is guided to embody the detected emotion when generating responses making them more personalized and emotionally expressive.

## Emotion Detection

We fine-tuned a BERT model using a dataset of over 30,000 labeled texts to categorize input into one of six emotion labels:

0: sadness 1: joy 2: love 3: anger 4: fear 5: surprise

For the second version of the Detection model, the Gemma 2 2B model was fine-tuned with over 400,000 labeled texts for enhanced emotion detection.

Both models (BERT or Gemma) can be used to implement emotion detection for the response model.

## Emotion-Based Responses

Once the core emotion is detected, a second model generates a response from the perspective of a character embodying that emotion. For the Response model, the Gemma 2 2B model was tuned with Unsloth and LoRA techniques, ensuring it produces responses that are emotionally rich and character-driven.

For example, when the detected emotion is sadness, the model generates an empathetic response by adopting the persona of "Sadness" itself. In terms of techniques, we identified specific functions and tuned hyperparameters to ensure the model produced the desired emotional output.

This approach enhances the model's ability to deliver emotionally accurate and personalized responses, effectively capturing the essence of the detected emotion.

Below is an example of some of the prompting strategies we used:

![image](https://github.com/user-attachments/assets/57e23d49-8bcd-44b1-a937-651f90989c5d)


One example of the model's output is shown below. Let's say you input: "The weather is perfect today! It's been months since I last felt this cool air!" The model will automatically detect the emotion (in this case, joy) and adopt the persona of the detected emotion (joy) to respond as follows:

![image](https://github.com/user-attachments/assets/a718266b-92a3-4d7b-9352-ef16e42537e3)

You can find the full original project here :

Code is accessible on Kaggle and Huggingface: https://www.kaggle.com/code/jiyoungleea/unsloth-final-version

Referece :

https://huggingface.co/unsloth/gemma-2-2b

https://velog.io/@judy_choi/Unsloth

https://www.datacamp.com/tutorial/fine-tuning-gemma-2

Created by Jiyoung Lee, Jeein Yang and Yoojin Kim.
