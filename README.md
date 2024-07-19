# SemEval-2024 Task 3: The Competition of Multimodal Emotion Cause Analysis in Conversations

## Abstract
We present a sub-task from Sem Eval-2023 Task 3, a shared task on extracting Textual emotion-cause pair extractions in conversations.This dataset consists of  conversations involving multiple people. Each dialogue in the conversation is annotated with the corresponding emotion - neutral, joy, sadness, anger, surprise, disgust, and fear. Every utterance with a nonneutral emotion has causal spans within the conversation. The task of participating systems was to predict the emotion of each utterance in a set of conversations and also predict the causal spans within the conversation. We are a group of three who took part in this task. We present our findings and results in this paper. In the end, the best-performing model for emotion classification achieved a macro F1 score of 0.47 on the validation set while the proportional span match F1 score for the span detection model was 0.6.

## Introduction 
Finding relationships between a pair of texts within a given context requires an understanding of the entire context and the contextual relationships between the pair. Extracting this information is particularly useful for conversational data. The emotion cause pair extraction has potential in areas of automated conflict resolution, therapeutic conversational agents, and marketing research. The task presented in the SemEval task is broken into two sub-tasks. As a first step, every utterance in the conversation is assigned an emotion based on the probability of each emotion associated with the text. This sub-task is followed by emotioncause span extraction aimed at extracting the span within the conversation. One of our approaches, however, tried to do both the sub-tasks in a single model. However, the final solution we present is a two-model-based approach. Due to the scarcity of training data, we relied on fine-tuning Bert models that were pre-trained on similar tasks.


## Data for training
Every instance in training data is a conversation involving multiple speakers. Each utterance is annotated with the speaker and an annotation. Every utterance in the conversation with an emotion other than neutral is annotated with a list of spans from all the utterances in the conversation. These spans are usually from the utterances before the target utterance and the target utterance but there are cases with the span being from a future utterance in cases with the same speaker.

![image](https://github.com/user-attachments/assets/279551ed-27e0-404d-8f12-79768cbe6a2b)


## Results 
![image](https://github.com/user-attachments/assets/cd770e28-95a0-438f-936d-b04d6db9b283)
