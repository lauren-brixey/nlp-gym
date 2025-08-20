# NLP-Based Topic Modelling for Gym Review Analysis

This project applies Natural Language Processing (NLP) techniques to uncover key customer pain points in online gym reviews. By analyzing real-world customer feedback from Google and Trustpilot, we identify recurring negative experiences and generate actionable insights for improving customer satisfaction at a commerical fitness chain.

---

## Project Overview

- **Objective**: Identify common causes of negative sentiment in customer reviews and provide strategic recommendations to improve the gym experience.
- **Dataset**: Thousands of 1–2 star reviews from Google and Trustpilot across gym locations.
- **Approach**: Combined traditional and modern NLP techniques (LDA, BERTopic, and LLMs) with emotion detection to extract, cluster, and interpret dominant complaint themes.

---

## Key Methods & Techniques

### 🔍 Data Preprocessing
- Filtered reviews for negative sentiment (<3 stars)
- Removed duplicates and non-English reviews
- Standard text cleaning: lowercasing, punctuation, and brand removal

### Topic Modelling
- **BERTopic**: Identified interpretable topic clusters across multiple data subsets
- **LDA (Baseline)**: Used for benchmarking model interpretability
- **LLM-Assisted Topic Extraction**: Employed Mistral-7B Instruct for fine-grained insights

### Emotion Detection
- Fine-tuned `bert-base-uncased` model used to filter reviews flagged as “anger”
- Focused topic modelling on emotionally charged complaints

---

## Results

- **Key pain points** identified:
  - Dirty or broken equipment
  - Poor customer service and rude staff
  - Overcrowding and gym access issues
  - Cold showers and air-conditioning failures
- **LLM-enhanced BERTopic** produced the most actionable and interpretable results
- **Actionable insights** included:
  - Improve equipment maintenance and cleaning protocols
  - Enhance staff training and professionalism
  - Redesign class schedules and gym layout for better crowd control
  - Simplify membership and pricing systems

---

## Tech Stack

- **Language**: Python
- **Libraries**: pandas, NumPy, scikit-learn, BERTopic, transformers, NLTK, gensim, matplotlib, seaborn
- **Models/Techniques**: BERTopic, LDA, Mistral-7B Instruct, Emotion Detection (BERT)

---

## Project Structure

```
├── notebooks/           # Jupyter notebooks for EDA, topic modelling, and LLM analysis
├── outputs/             # Visualizations and final topic clusters
├── report/              # Stakeholder-facing summary report (PDF)
├── README.md            # Project overview and documentation
```

---

## Conclusion

This project demonstrates how hybrid NLP techniques can be used to extract meaningful insights from large-scale unstructured text. The findings provide gyms with a roadmap to enhance customer satisfaction by addressing the most frequent and emotionally charged complaints across their locations.
