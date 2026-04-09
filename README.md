# Brand Visibility Dataset (BVDS)

This project explores how different ways of asking for product recommendations (prompt variations) affect the brands suggested by large language models (LLMs).

The goal is to understand whether models show patterns or preferences when recommending brands.

---

## 📁 Project Structure 📁

### Data Collection (API Scripts)

- **BVDS_Anthropic_API.py**  
- **BVDS_Google_API.py**

These scripts were used to generate the dataset.

They:
- Take products from `products.csv`
- Generate different prompt variations (e.g. “best”, “affordable”, etc.)
- Send those prompts to LLM APIs (Anthropic / Google)
- Collect responses
- Extract brand names using the `BRANDS: [...]` format
- Store results in a structured dataset

---

### Raw Product Input

- **products.csv**

Contains:
- 4 categories
- 25 products per category

This is the base used to generate all prompts.

---

### Final Dataset

- **brands_data_complete.csv**

This is the **main dataset** used for analysis.

It includes:
- Prompt text  
- Product and category  
- Model used  
- Full response  
- Extracted brands  
- Brand counts  

---

### Preprocessing & Visualisation

- **preprocessing_and_visualizing.py**

This script:
- Cleans and prepares the dataset
- Creates visualisations (e.g. brand frequency, distributions)
- Helps identify patterns in the data


---

### Machine Learning

- **ml_on_bvds.py**

This script applies basic machine learning techniques, including:
- Clustering (K-Means)
- Pattern discovery in brand counts and prompt types

 In simple terms:  
**This is where we test if the dataset shows meaningful patterns**

---

## Pipeline Overview

The project follows this workflow:

1. Select products and categories (`products.csv`)  
2. Generate prompts automatically  
3. Send prompts to LLM APIs (Anthropic & Google)  
4. Collect responses  
5. Extract brands into structured format  
6. Merge datasets  
7. Clean and visualise data  
8. Apply machine learning for analysis  

---

## ⚠️ Notes ⚠️ 

- Results depend on model behaviour at the time of data collection  
- Outputs may reflect biases from the models themselves  
- API keys are required to run the data collection scripts  
