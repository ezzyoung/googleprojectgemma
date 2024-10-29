<<<<<<< HEAD
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
=======
---
base_model: unsloth/gemma-2-2b
library_name: peft
---

# Model Card for Model ID

<!-- Provide a quick summary of what the model is/does. -->



## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->



- **Developed by:** [More Information Needed]
- **Funded by [optional]:** [More Information Needed]
- **Shared by [optional]:** [More Information Needed]
- **Model type:** [More Information Needed]
- **Language(s) (NLP):** [More Information Needed]
- **License:** [More Information Needed]
- **Finetuned from model [optional]:** [More Information Needed]

### Model Sources [optional]

<!-- Provide the basic links for the model. -->

- **Repository:** [More Information Needed]
- **Paper [optional]:** [More Information Needed]
- **Demo [optional]:** [More Information Needed]

## Uses

<!-- Address questions around how the model is intended to be used, including the foreseeable users of the model and those affected by the model. -->

### Direct Use

<!-- This section is for the model use without fine-tuning or plugging into a larger ecosystem/app. -->

[More Information Needed]

### Downstream Use [optional]

<!-- This section is for the model use when fine-tuned for a task, or when plugged into a larger ecosystem/app -->

[More Information Needed]

### Out-of-Scope Use

<!-- This section addresses misuse, malicious use, and uses that the model will not work well for. -->

[More Information Needed]

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

[More Information Needed]

### Recommendations

<!-- This section is meant to convey recommendations with respect to the bias, risk, and technical limitations. -->

Users (both direct and downstream) should be made aware of the risks, biases and limitations of the model. More information needed for further recommendations.

## How to Get Started with the Model

Use the code below to get started with the model.

[More Information Needed]

## Training Details

### Training Data

<!-- This should link to a Dataset Card, perhaps with a short stub of information on what the training data is all about as well as documentation related to data pre-processing or additional filtering. -->

[More Information Needed]

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Preprocessing [optional]

[More Information Needed]


#### Training Hyperparameters

- **Training regime:** [More Information Needed] <!--fp32, fp16 mixed precision, bf16 mixed precision, bf16 non-mixed precision, fp16 non-mixed precision, fp8 mixed precision -->

#### Speeds, Sizes, Times [optional]

<!-- This section provides information about throughput, start/end time, checkpoint size if relevant, etc. -->

[More Information Needed]

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data, Factors & Metrics

#### Testing Data

<!-- This should link to a Dataset Card if possible. -->

[More Information Needed]

#### Factors

<!-- These are the things the evaluation is disaggregating by, e.g., subpopulations or domains. -->

[More Information Needed]

#### Metrics

<!-- These are the evaluation metrics being used, ideally with a description of why. -->

[More Information Needed]

### Results

[More Information Needed]

#### Summary



## Model Examination [optional]

<!-- Relevant interpretability work for the model goes here -->

[More Information Needed]

## Environmental Impact

<!-- Total emissions (in grams of CO2eq) and additional considerations, such as electricity usage, go here. Edit the suggested text below accordingly -->

Carbon emissions can be estimated using the [Machine Learning Impact calculator](https://mlco2.github.io/impact#compute) presented in [Lacoste et al. (2019)](https://arxiv.org/abs/1910.09700).

- **Hardware Type:** [More Information Needed]
- **Hours used:** [More Information Needed]
- **Cloud Provider:** [More Information Needed]
- **Compute Region:** [More Information Needed]
- **Carbon Emitted:** [More Information Needed]

## Technical Specifications [optional]

### Model Architecture and Objective

[More Information Needed]

### Compute Infrastructure

[More Information Needed]

#### Hardware

[More Information Needed]

#### Software

[More Information Needed]

## Citation [optional]

<!-- If there is a paper or blog post introducing the model, the APA and Bibtex information for that should go in this section. -->

**BibTeX:**

[More Information Needed]

**APA:**

[More Information Needed]

## Glossary [optional]

<!-- If relevant, include terms and calculations in this section that can help readers understand the model or model card. -->

[More Information Needed]

## More Information [optional]

[More Information Needed]

## Model Card Authors [optional]

[More Information Needed]

## Model Card Contact

[More Information Needed]
### Framework versions

- PEFT 0.13.0
>>>>>>> bb85acd (Initial commit)
