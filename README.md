# on-policy distillation (opd)
<a target="_blank" href="https://colab.research.google.com/github/andrewgcodes/onpolicydistillation/blob/main/on_policy_distillation.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

In this Colab notebook, you'll do on-policy distillation (OPD) on Qwen3-0.6b using Qwen3-4b-Instruct-2507, to make it better at [GSM8K](https://huggingface.co/datasets/openai/gsm8k) (a dataset of math problems).

Unlike standard supervised fine-tuning (SFT), the student model (Qwen-3-0.6b) learns from its own generated outputs rather than fixed gold data — reducing exposure bias and better matching the inference-time distribution.

You'll need to connect an A100 GPU (40 GB Ram) or better. You might be able to get away with smaller GPUs if you change some of the config parameters, like samples_per_prompt and max_new_tokens!

Inspired by [Thinking Machines](https://thinkingmachines.ai/blog/on-policy-distillation/) and prior art like [Agarwal et al](https://arxiv.org/abs/2306.13649).
