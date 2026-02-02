# Sentiment Analysis of Financial Text

## Objective
Analyze sentiment of financial text using 3-class classification with the purpose of eventually deploying the model to analyze daily news on particular topics or equities.
Model development was a part of a Master's course in 2025.

## Model Overview
Tested multiple techniques model tuning techniques, including LoRA and prompt tuning. Tested predefined and custom benchmarks on Llama 3 and GPT 2. Benchmarks were evaluated on gpt2-open-instruct-v1 because of resource constraints when evaluating llama 3 8B or 70B instruct models.

## Benchmarks
Tested multiple benchmarks from multifin. Developed a custom benchmark to compute the proximity of the model's response to the correct answer. For example, if the true label "positive", then an assigned label of "neutral" is punished less than an assigned label of "negative".

## Training data used for few-shot prompting
financial dataset: https://huggingface.co/datasets/warwickai/financial_phrasebank_mirror 

## Outcome
Prompt tuning improved the performance on the custom benchmark by 20%, although additional model development and GPU resources are needed before deployment. Evaluation should be conducted on larger Llama 3 - instruct models. 
