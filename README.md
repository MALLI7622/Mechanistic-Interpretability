# Mechanistic-Interpretability

The study I have conducted investigates how fine-tuning a large language model (LLM) for medical reasoning alters its internal representations and output distributions between the fine-tuned and base model (Model Diffing). Using DeepSeek-R1-Distill-Qwen-1.5B, fine-tuned the model with Low-Rank Adaptation (LoRA) on a medical reasoning dataset(FreedomIntelligence/HuatuoGPT-o1-8B
). The study quantifies how much the fine-tuned model diverges from the pretrained model, identifying which layers encode domain-specific knowledge. I have used Kullback-Leibler (KL) divergence to measure changes in output probabilities and activation patching (resources provided by Neel has helped me a lot to better understand the code and theory) to analyze how swapping specific layers affects responses.

The study I have conducted investigates how fine-tuning a large language model (LLM) for medical reasoning alters its internal representations and output distributions between the fine-tuned and base model (Model Diffing). Using DeepSeek-R1-Distill-Qwen-1.5B, fine-tuned the model with Low-Rank Adaptation (LoRA) on a medical reasoning dataset(FreedomIntelligence/HuatuoGPT-o1-8B
). The study quantifies how much the fine-tuned model diverges from the pretrained model, identifying which layers encode domain-specific knowledge. I have used Kullback-Leibler (KL) divergence to measure changes in output probabilities and activation patching (resources provided by Neel has helped me a lot to better understand the code and theory) to analyze how swapping specific layers affects responses.

## Key Findings in the study
1. Fine-tuning effectively imparts medical reasoning ability
2. KL divergence analysis reveals substantial distribution shifts, particularly on medical terms and explanation-heavy answers.
3. Activation patching experiments identify key layers responsible for domain adaptation, showing that fine-tuning predominantly alters higher-level transformer layers.
