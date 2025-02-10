# **Task Extraction and Sentiment Analysis**

This repository contains the implementation of two tasks:
1. **Part A**: Extract and categorize tasks from unstructured text using an NLP pipeline.
2. **Part B**: Build a machine learning model to classify customer reviews as positive or negative.
## **Part A: Task Extraction and Categorization**
### **Objective**
The goal is to create an NLP pipeline that identifies and categorizes tasks from unstructured text. The pipeline extracts:
- The task 
- The person responsible 
- The deadline
### **Steps**
1. **Preprocessing**:
   - Clean the text (remove stop words, punctuation, and irrelevant metadata).
   - Tokenize sentences and perform POS tagging.
2. **Task Identification**:
   - Use heuristics to identify sentences representing tasks.
   - Extract actionable verbs, responsible persons, and deadlines.
3. **Categorization**:
   - Use TF-IDF and Latent Dirichlet Allocation (LDA) to cluster tasks into categories.
4. **Output**:
   - Generate a structured list of tasks with categories, responsible persons, and deadlines.
### **Code Structure**
- `preprocess_text(text)`: Cleans and tokenizes the input text.
- `identify_tasks(doc)`: Identifies tasks using heuristics.
- `categorize_tasks(task_texts)`: Clusters tasks into categories using LDA.
- `generate_output(tasks, categories)`: Generates a structured output.

### Input
```text
Rahul wakes up early every day. He goes to college in the morning and comes back at 3 pm. At present, Rahul is outside. He has to buy the snacks for all of us.
[
### Output
  {
    "task": "buy",
    "who": "Rahul",
    "deadline": null,
    "category": 1
  }
]
