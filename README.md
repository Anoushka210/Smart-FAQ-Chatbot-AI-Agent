# Smart FAQ Chatbot AI Agent

**Applied Artificial Intelligence Project**  

---

##  Project Overview

This project implements a **retrieval-based AI chatbot** designed to automate **Frequently Asked Questions (FAQ)** support.  
Unlike generative models (such as GPT), this agent relies on **TF-IDF (Term Frequency–Inverse Document Frequency)** and **Cosine Similarity** to accurately map user queries to a predefined knowledge base, ensuring **factual, consistent, and deterministic responses**.

The system also includes a **hybrid engine** capable of handling both **technical queries** and **small talk**, resulting in a more natural user experience.

---

##  Objectives

- **Intelligent Retrieval**  
  Implement TF-IDF vectorization to convert text into numerical representations.

- **Similarity Matching**  
  Use Cosine Similarity to identify the closest matching FAQ entry.

- **Hybrid Response System**  
  Combine:
  - Machine Learning–based retrieval for FAQs  
  - Rule-based logic for greetings and small talk

- **Performance Analytics**  
  Visualize chatbot accuracy and confidence scores using Matplotlib and Seaborn.

- **Threshold Gating**  
  Apply a confidence threshold (e.g., `< 50%`) to gracefully handle unknown or irrelevant queries.

---

##  Technologies Used

- **Language:** Python  
- **NLP & Machine Learning:**  
  - `scikit-learn` (TfidfVectorizer, cosine_similarity)  
  - `re` (Regular Expressions)
- **Data Processing:** `numpy`  
- **Visualization:** `matplotlib`, `seaborn`

---

##  How It Works

1. **Preprocessing**  
   - User input is cleaned (lowercased, special characters removed).

2. **Vectorization**  
   - User queries and the FAQ knowledge base are converted into TF-IDF vectors.

3. **Similarity Calculation**  
   - Cosine similarity is computed between the user query and all stored FAQs.

4. **Response Selection**
   - If a *small talk* pattern is detected (e.g., "Hi", "Bye"), the chatbot responds immediately.
   - Otherwise, the FAQ with the **highest similarity score** is returned.
   - If the highest score falls below the defined threshold, a fallback response is returned:
     > _"I'm not sure about that..."_

---

##  Usage

### Running the Chatbot

```bash
# 1 Install dependencies
pip install scikit-learn numpy matplotlib seaborn

# 2 Run the script
python FAQ_AI_Chatbot.py
