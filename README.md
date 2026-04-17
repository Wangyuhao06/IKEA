# IKEA (**I**mplicit **K**nowledge **E**xtraction **A**ttack)
The code of the following paper will be released in this repository:

[**Silent Leaks: Implicit Knowledge Extraction Attack on RAG Systems through Benign Queries**](https://arxiv.org/pdf/2505.15420) .


📦 **Setup Instructions**

Follow the steps below to set up and run the pipeline.

🔐 **1. Environment Configuration**

Create a `.env` file in the root directory to store your API keys. This is required for accessing OpenAI and DeepSeek models.

Add the following lines to the .env file:
```bash
OPENAI_KEY=your_openai_api_key
DEEPSEEK_KEY=your_deepseek_api_key
```
📁 **2. Dataset Preparation**

Download one or more of the following datasets from Hugging Face and place them into the datasets/ directory:
- [ChatDoctor-HealthCareMagic-100k](https://huggingface.co/datasets/lavita/)
- [HarryPotterQA](https://huggingface.co/datasets/vapit/HarryPotterQA)
- [PokemonQA](https://huggingface.co/datasets/tungdop2/pokemon)

Example folder structure:

datasets/

├── ChatDoctor-HealthCareMagic-100k.json

├── HarryPotterQA.json

├── PokemonQA.json

**Note:** Ensure each dataset is saved in a valid JSON format, i.e., a list of objects with {"input": ..., "output": ...} structure.

▶️ **3. Run the Pipeline**

Execute the main feedback mutation pipeline script:
```bash
python feedback_mutation_pipeline.py
```

📌 **Note:**
- API usage may incur costs depending on the number of queries issued
- Output logs and extracted results will be saved in the outputs/ directory

## Citation

```bibtex
@article{wang2025silent,
  title={Silent leaks: Implicit knowledge extraction attack on rag systems through benign queries},
  author={Wang, Yuhao and Qu, Wenjie and Zhai, Shengfang and Jiang, Yanze and Liu, Zichen and Liu, Yue and Dong, Yinpeng and Zhang, Jiaheng},
  journal={arXiv preprint arXiv:2505.15420},
  year={2025}
}
```
