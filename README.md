# dialog-summarization-using-llms
Dialog Summarization using FLAN-T5 with different Fine-Tuning techniques


## 1. Fine-Tuning FLAN-T5 Model for Dialog Summarization using Prompt Engineering
- Dataset used >> DialogSum: A Real-Life Scenario Dialogue Summarization Dataset (https://doi.org/10.48550/arXiv.2105.06762).
- Zero Shot Inference with an Instruction Prompt.
- Zero Shot Inference with the Prompt Template from FLAN-T5.
- One Shot Inference.
- Few Shot Inference.
- Few Shot Inference with updates to Generation Config.


## 2. Fine-Tuning FLAN-T5 Model for Dialog Summarization using PEFT (LoRA)
- Dataset used >> DialogSum.
- Full fine-tuning (instruction fine tuning).
- Parameter-Efficient Fine-Tuning using LoRA (Low-Rank Adaptation).
- Quantitative evaluation of model using ROUGE metric.


## 3. Fine-Tune FLAN-T5 with Reinforcement Learning (PPO) and PEFT to Generate Less-Toxic Summaries
- Dataset used >> DialogSum.
- Prepare Reward Model - RoBERTa-based hate speech model (https://huggingface.co/facebook/roberta-hate-speech-dynabench-r4-target).
- Get the query responses from the policy LLM (PEFT model).
- Compare responses from the Reference Model and Policy Model.
- Calculate KL Divergence.
- Get sentiments (reward logits) for query/responses from hate speech RoBERTa model.
- Optimize policy with PPO using the (query, response, reward) triplet.
  (Policy Optimization - Minimise KL Divergence, Maximize Mean Returns, Maximize Advantages).
- Quantitative evaluation of model using Toxicity Evaluation Metric (https://huggingface.co/spaces/evaluate-measurement/toxicity).
