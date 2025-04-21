# 🦙 LLaMA-2 PEFT Fine-Tuning with LoRA and 4-bit Quantization

This project demonstrates parameter-efficient fine-tuning (PEFT) of the 7B LLaMA-2 chat model using **LoRA (Low-Rank Adaptation)** and **4-bit quantization** via **BitsAndBytes**, built on top of Hugging Face's `transformers`, `peft`, and `datasets` libraries.

The model is fine-tuned on a curated subset of the [OpenAssistant-Guanaco](https://huggingface.co/datasets/timdettmers/openassistant-guanaco) dataset, containing high-quality multi-turn conversational samples.

---

## 📌 Project Highlights

- **Model:** LLaMA-2-7B-Chat (`NousResearch/Llama-2-7b-chat-hf`)
- **Technique:** Parameter-Efficient Fine-Tuning using LoRA
- **Quantization:** 4-bit (NF4) with `bitsandbytes`
- **Libraries Used:** Hugging Face `transformers`, `peft`, `datasets`, `bitsandbytes`
- **Training Framework:** `SFTTrainer` from Hugging Face
- **Hardware:** Trained on Kaggle GPU (Tesla P100, 16GB)
- **Performance:** Achieved training loss of **0.80** in 75 steps

---

## 🚀 Hosted Model

The fine-tuned LoRA adapters have been uploaded and are publicly available on the Hugging Face Hub:

🔗 [**View Model on Hugging Face**](https://huggingface.co/Blackmoonbear/llama2-peft-openassistant)

You can load the model directly using:

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model = AutoModelForCausalLM.from_pretrained("your-username/llama2-peft-openassistant")
tokenizer = AutoTokenizer.from_pretrained("your-username/llama2-peft-openassistant")

```
