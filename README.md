# The Budget AI Researcher and the Power of RAG Chains
Navigating the vast and rapidly growing body of scientific literature is a formidable challenge for aspiring researchers. Current approaches to supporting research idea generation often rely on generic large language models (LLMs). While LLMs are effective at aiding comprehension and summarization, they often fall short in guiding users toward practical research ideas due to their limitations. In this study, we present a novel structural framework for research ideation. Our framework, The Budget AI Researcher, uses retrieval-augmented generation (RAG) chains, vector databases, and topic-guided pairing to recombine concepts from hundreds of machine learning papers. The system ingests papers from nine major AI conferences, which collectively span the vast subfields of machine learning, and organizes them into a hierarchical topic tree. It uses the tree to identify distant topic pairs, generate novel research abstracts, and refine them through iterative self-evaluation against relevant literature and peer reviews, generating and refining abstracts that are both grounded in real-world research and demonstrably interesting. Experiments using LLM-based metrics indicate that our method significantly improves the concreteness of generated research ideas relative to standard prompting approaches. Human evaluations further demonstrate a substantial enhancement in the perceived interestingness of the outputs. By bridging the gap between academic data and creative generation, the Budget AI Researcher offers a practical, free tool for accelerating scientific discovery and lowering the barrier for aspiring researchers. Beyond research ideation, this approach inspires solutions to the broader challenge of generating personalized, context-aware outputs grounded in evolving real-world knowledge.

**Author**: Franklin Lee  
**Co-Author**: Tengfei Ma  
**Affiliations**: Jericho Senior High School, Stony Brook University  
**DOI**: [10.1109/ACCESS.2024.0429000](https://doi.org/10.1109/ACCESS.2024.0429000)

## Overview

The Budget AI Researcher is a free and extensible Python-based system designed to accelerate scientific discovery. It leverages Retrieval-Augmented Generation (RAG), vector databases, and large language models (LLMs) to generate, evaluate, and refine novel research ideas grounded in real-world academic literature.

This project lowers the barrier to entry for students and independent researchers who wish to explore machine learning research without the need for expensive APIs or proprietary datasets.

## Features

- Retrieval-Augmented Generation (RAG) pipeline using ChromaDB and LangChain
- Topic tree construction from 9 major AI conferences
- Abstract generation by recombining distant AI topics
- Semantic Scholar API integration for citation-based refinement
- OpenReview scraping for peer-review-based abstract polishing
- Summarization and Q&A capabilities based on ingested papers
- Evaluation through both LLM metrics and human reviewers

## System Architecture

1. Ingests papers from 9 top AI conferences (e.g., NeurIPS, ICML, ACL)
2. Extracts and vectorizes text using LangChain and ChromaDB
3. Clusters research into topic trees via LLM prompting
4. Identifies distant topic pairs to generate novel abstracts
5. Uses Semantic Scholar and OpenReview for citation-based evaluation
6. Provides summarization and question-answering utilities

## Conferences Used

- NeurIPS
- ICML
- ICLR
- ACL
- EMNLP
- NAACL
- CVPR
- ECCV
- ICCV

## Repository Contents

- `The Budget AI Researcher and the Power of RAG Chains.ipynb`: Main implementation notebook
- `Main Manuscript.pdf`: Full IEEE-style research manuscript
- `requirements.txt`: Dependencies for running the notebook

## Installation

Install dependencies using pip:

pip install -r requirements.txt

Run the notebook:

jupyter lab
# or
jupyter notebook

Example Use Cases
Summarization: Generate 100-word summaries of complex machine learning papers

Topic Tree Construction: Automatically categorize papers into topics like prompt engineering, LLM reasoning, and adversarial attacks

Abstract Generation: Create novel research paper abstracts by recombining concepts from distant topics

Question Answering: Ask questions like "What is federated learning?" using real ML paper embeddings as context

### Quantitative Performance (LLM-Based)

| Model                | Interestingness | Novelty | Feasibility |
|----------------------|----------------|---------|-------------|
| GPT-4o-mini          | 8.40           | 7.55    | 7.80        |
| LLaMA 3.2 90B        | 8.15           | 7.30    | 7.70        |
| Claude 3.5           | 8.05           | 7.30    | 7.55        |
| Budget AI Researcher | 8.37           | 8.13    | 7.89        |

### Human Evaluation

| Metric          | AI Scientist | Budget AI Researcher |
|-----------------|-------------|---------------------|
| Interestingness | 2.93        | 3.58                |
| Feasibility     | 3.57        | 3.55                |
| Novelty         | 3.28        | 3.23                |

Citation
If you use this system or reference the manuscript in your work, please cite:

@article{lee2024budget,
  title={The Budget AI Researcher and the Power of RAG Chains},
  author={Franklin Lee and Tengfei Ma},
  journal={IEEE Access},
  year={2024},
  doi={10.1109/ACCESS.2024.0429000}
}
Contact
Franklin Lee: franklin.lee@stonybrook.edu

Tengfei Ma: tengfei.ma@stonybrookmedicine.edu

License
This project is released for academic use. Licensing for commercial use is not included. Contact the authors for inquiries.
