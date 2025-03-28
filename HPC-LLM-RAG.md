# 🚀✨ **HPC: Introduction to Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) for Beginners** ✨🚀  


## 🎯 **Goal**  
🤖 **Learn how to efficiently use Large Language Models (LLMs) with Retrieval-Augmented Generation (RAG) on CSUSB HPC to improve accuracy by integrating external knowledge retrieval.
Traditional LLMs struggle with retrieving up-to-date information. **RAG enhances LLMs** by integrating external knowledge retrieval, improving accuracy for tasks like answering complex queries.  

---

## 📌 **What You Will Learn** 🧠💡  
- ✅ **Use CSUSB’s High-Performance Computers (HPC) to run AI faster 💨**
- ✅ **Train an AI model that retrieves real facts before answering 🧠** 
- ✅ **Build your own AI system that improves response accuracy 💡**
- ✅ **Why use a High-Performance Computing (HPC) instead of a personal computer?**  
- ✅ **How to set up your environment and Install Dependencies, Setup Kaggle, and Download Dataset**   
- ✅ **Load and Preprocess the Dataset in Jupyter Notebook**  
- ✅ **Implementing Retrieval-Augmented Generation (RAG)**  
- ✅ **Analyzing Retrieval Efficiency**  

---

## 🚀 **1. 🤖 What is Retrieval-Augmented Generation (RAG)?


## 📌 **Introduction**
🔹 Retrieval-Augmented Generation (RAG) is an AI framework that enhances **Large Language Models (LLMs)** by integrating **real-time knowledge retrieval** with text generation. Instead of relying solely on pre-trained knowledge, RAG retrieves **relevant external documents 📚** to provide **more accurate, context-aware responses**.

Example:
 - 🏆 Basic AI: "The latest iPhone is the iPhone 14." ❌ (Might be outdated!)
 - 💡 RAG AI: "The latest iPhone is the iPhone 15, released in 2023." ✅ (Checked real sources!)


## 🏗 **RAG System Architecture**
### 📊 **Workflow Diagram**

<img src="https://github.com/user-attachments/assets/acab4adb-8f41-46ed-8cb6-d5d11ab2c072" width="550">

Source: [What is Retrieval-Augmented Generation?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)

## ⚙️ **How RAG Works (Aligned with Diagram)**
### 🔹 **Key Processing Steps**
1️⃣ **User Input 💬** → The user provides a **query** (e.g., a question or request for information).<br>
2️⃣ **Query Sent to Retrieval System 🔎** → The system searches an external **knowledge base 📂** for relevant information.<br>
3️⃣ **Relevant Documents Retrieved 📖** → The system finds the most **contextually relevant documents** and extracts useful content.<br>
4️⃣ **Enhanced Context Generation 📝** → The **retrieved information is merged** with the original query, creating an enriched prompt.<br>
5️⃣ **LLM Generates Response 🧠** → The **augmented prompt** is sent to the language model to generate a **fact-based answer**.<br>
6️⃣ **Final Response ✅** → The user receives a response **grounded in retrieved knowledge**.<br>

### 🔍 **Core Components (Matching Workflow Elements)**
| **Component**                | **Function** |
|------------------------------|-------------|
| **User Query** 💬           | Initial question or request for information |
| **Search Relevant Information** 🔍 | Finds matching knowledge in external sources |
| **Knowledge Sources** 📚      | Databases, documents, or repositories storing retrievable data |
| **Retrieved Context** 📄     | Relevant snippets extracted for augmentation |
| **Enhanced Prompt** ✍️      | Merged user query + additional context |
| **LLM Processing** 🧠        | Generates responses using both pre-trained knowledge and retrieved content |


## 🎯 **Why Use RAG?**
✔ **Reduces Hallucination 🚫** – Retrieves **real-time information** instead of making assumptions.  
✔ **More Context-Aware 📌** – Uses retrieved data to **enhance LLM responses**.  
✔ **Scalable & Efficient ⚡** – Works with **large document repositories** without retraining the model.  
✔ **Improves Accuracy 🎯** – Ensures answers **align with verified sources**.  

**🔹 4. How Does RAG Work? (Step by Step)**
Let’s say you want to know “Who won the last World Cup?”

💡 RAG follows these steps:

- 1️⃣ You ask the question 🗣 → "Who won the last World Cup?"
- 2️⃣ AI searches the web 🔍 → It looks for recent sports news!
- 3️⃣ AI finds the answer 📚 → Finds an article from 2022.
- 4️⃣ AI combines knowledge 📝 → Uses both old training + new info.
- 5️⃣ AI gives a fact-based answer ✅ → "Argentina won the 2022 FIFA World Cup."
 
🔍 **Without RAG:**
- The LLM might generate an **outdated response** based only on its last training data.

✅ **With RAG:**
- The system **retrieves recent research papers 📰** and trusted articles.
- The model **incorporates external knowledge**, ensuring a **current and factual answer**.

## 🏁 **Conclusion**
By combining **retrieval** with **generation**, RAG **significantly improves response accuracy** by grounding LLM outputs in real-world information. This framework is **widely used** in applications like **intelligent search engines 🔍, enterprise AI assistants 🤖, and automated research tools 📊**.


## 🖥️ **1. Why Use HPC Instead of a Local Computer?**

💡 Think of it like playing video games on an old vs. a new console!
🚗 Local computer (like a normal laptop) 
 - Slow processing (like running a new game on an old PlayStation)
 - Limited memory (can’t handle big AI models)
 - Takes HOURS to process large data

🚀 HPC (Super-powerful computers in a lab!)
 - Faster! Can process HUGE amounts of information in minutes
 - Has better GPUs (graphics processing units) for AI tasks
 - Can handle more data at once

📌 Example:
 - Running AI on a regular laptop = Waiting 5 hours 🕰
 - Running AI on HPC = Done in 5 minutes ⚡


---

## 🔍 **2: Access HPC Terminal via CSUSB HPC Portal**

Once you sign in to the CSUSB HPC portal, follow these steps to configure and launch your server:

### Step 1: Access the HPC JupyterHub   
1️⃣ Log into [CSUSB HPC Portal](https://csusb-hpc.nrp-nautilus.io/) using your school credentials.   
2️⃣ Click CI Logon and authenticate.  

### Step 2: Configure Your Server   
1️⃣ Click Start My Server or Launch Server if prompted.   
2️⃣ Under Advanced Options, adjust the following:   

- GPUs: 2
- GPU Type: Leave as Any
- Cores: 4 (default)
- RAM: 16 GB (default)
 
3️⃣ Under Image, select:   
✅ Stack Datascience   
### Step 3: Start Your Server   
1️⃣ Scroll down and click Start to launch the server.   
2️⃣ Wait for the server to initialize. Once it is ready, JupyterHub will open in a new tab.

✅ Now your server is ready for the workshop! 🚀

---

## 💻 **3. Install Dependencies, Setup Kaggle, and Download Dataset**

1️⃣ Click **Terminal** in JupyterLab.    
2️⃣ Run the following commands:    

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1712-6940-8004-9dd6-df6e5b2542c1)

```bash
# Install Pandas, a powerful library for data manipulation and analysis, 
# providing data structures like DataFrames for handling structured data.
pip install --user pandas  

# Install Seaborn, a statistical data visualization library built on top of Matplotlib, 
# useful for creating informative and attractive graphs.
pip install --user seaborn  

# Install Matplotlib, a fundamental plotting library for Python, 
# enabling the creation of static, animated, and interactive visualizations.
pip install --user matplotlib  

# Install the Kaggle API library, which allows users to download datasets, 
# submit solutions, and interact with Kaggle’s platform programmatically.
pip install --user kaggle  

# Install FAISS (Facebook AI Similarity Search), an efficient library for 
# similarity search and clustering of dense vectors, optimized for fast retrieval.
pip install --user faiss-cpu  

# Install Hugging Face's Transformers library, which provides pre-trained models 
# for various NLP tasks such as text classification, translation, and generation.
pip install --user transformers   

# Temporarily add Kaggle to your system PATH
export PATH=~/.local/bin:$PATH  

# Permanently add Kaggle to your system PATH
echo 'export PATH=~/.local/bin:$PATH' >> ~/.bashrc  

# Apply the changes immediately
source ~/.bashrc  

# Create a new directory for dataset storage
mkdir -p ~/playstore_data  

# Navigate to dataset directory
cd ~/playstore_data  

# Download the Google Playstore dataset from Kaggle
kaggle datasets download -d gauthamp10/google-playstore-apps  

# Unzip the downloaded dataset
unzip google-playstore-apps.zip  

# List extracted files to confirm successful download
ls -lh  

```
Simple Breakdown of what each download does:
 - pandas → Handles large datasets 📊
 - seaborn & matplotlib → Create charts 📈
 - kaggle → Download datasets 📥
 - faiss-cpu → Fast document searching 🔍
 - transformers → AI models 🤖


3️⃣ **Click Run (▶) and check the output!** 

✅ **Now you have installed dependencies and downloaded the dataset! 🎉**

---

## 📚 **4: Load and Preprocess the Dataset in Jupyter Notebook**

## Step 1: Load the Dataset into a Pandas DataFrame 
   
### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1d6c-9c98-8004-8d4e-71cacaa3d24d)    

```python
# Import Pandas for data handling
import pandas as pd  

# Define dataset path
dataset_path = "~/playstore_data/Google-Playstore.csv"  

# Load dataset into Pandas DataFrame
playstore_df = pd.read_csv(dataset_path)  

# Display first few rows
print(playstore_df.head())  
```
3️⃣ Click **Run** (▶) and check the output.

✅ **You should now see your dataset displayed!** 🎉

## Step 2: Clean and Prepare Data for RAG    

### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1dbe-8580-8004-8d58-e95625a51e73)    

```python
# Check for missing values in the dataset
missing_values = playstore_df.isnull().sum()  
print("Missing Values:\n", missing_values)  

# Remove missing values
playstore_df.dropna(inplace=True)  

# Remove duplicate entries
playstore_df.drop_duplicates(inplace=True)  

# Display cleaned dataset
print(playstore_df.head())  
```
3️⃣ Click **Run** (▶) and check the output.

✅ **Now your dataset is clean and ready for retrieval-augmented generation.**

---

## 🤖 **5. Implementing Retrieval-Augmented Generation (RAG)**

## Step 1: Install and Import Required Libraries    

### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:    

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1e19-a334-8004-b603-1f7d4a2034a2)    

```python
# Import required Hugging Face and FAISS libraries
from transformers import pipeline, RagTokenizer, RagRetriever, RagSequenceForGeneration  
import faiss  
```
3️⃣ Click **Run** (▶) to import the libraries.

✅ Libraries imported successfully! You're now ready to use RAG for retrieval-augmented generation. 🚀🎉

## Step 2: Load a Pre-Trained RAG Model 
   
### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1e75-6a94-8004-b865-f43171fe3604)    

```python
# Define tokenizer model name
tokenizer_model = "facebook/rag-sequence-nq"  

# Load tokenizer
tokenizer = RagTokenizer.from_pretrained(tokenizer_model)  

# Define generation model
generation_model = "gpt2"  

# Load text generation model
model = pipeline("text-generation", model=generation_model)  
```
3️⃣ Click **Run** (▶) to load the pre-trained model.

✅ Tokenizer and generation model loaded successfully! You're now ready to generate text with RAG and GPT-2. 🚀🎉

## Step 3: Define Query and Retrieve Information  
  
### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1ebe-2cf4-8004-98f1-4f71c9d6d1ab)    

```python
# Define a user query
query = "What are the top categories in Google Playstore?"  

# Tokenize query
input_dict = tokenizer.prepare_seq2seq_batch(query, return_tensors="pt")  

# Retrieval disabled since retriever is removed
retrieved_docs = None  
```

3️⃣ Click **Run** (▶) to retrieve information.

✅ Query tokenized successfully! Your input is now ready for processing. 🔍🎉

## Step 4: Generate a Response  
  
### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code: 
 
🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1f35-4c38-8004-b5dd-9f91a69c3fa2)    

```python
# Generate response based on retrieved documents
output = model(query, max_length=100, truncation=True)  

# Extract generated response
generated_response = output[0]['generated_text']  

# Print generated answer
print("Generated Answer:", generated_response)  
```
3️⃣ Click **Run** (▶) to generate a response.

✅ Response generated successfully! You should now see the AI-generated answer based on the query. 💡🎉

---

## 📊 **6: Analyzing Retrieval Efficiency**
    
### **➕🐍 Add a New Code Cell**    
1️⃣ Click **+ Code** in Jupyter Notebook to add a new code cell.  
2️⃣ Copy and paste the following code:  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cb1f85-ef38-8004-88b3-972f1e37ca9f)    

```python
# Import visualization libraries
import matplotlib.pyplot as plt  
import seaborn as sns  

# Set figure size for better visualization
plt.figure(figsize=(12, 5))  

# Create bar plot for app categories
sns.countplot(x=playstore_df["Category"])  

# Rotate x-axis labels for readability
plt.xticks(rotation=90)  

# Set title
plt.title("Distribution of App Categories in Google Playstore")  

# Display the plot
plt.show()  
```
3️⃣ Click **Run** (▶) and check the output.

✅ **You should see a distribution of app categories.**

<img src="https://github.com/user-attachments/assets/b1d73377-5b32-46de-9a8d-a38376673770" alt="Self-Service System" width="650">


---

## 🎯 **7. Wrap-Up & Next Steps**  
🎉 Congratulations! You learned how to:

- ✅ **Use HPC for Large-Scale Retrieval-Augmented Generation (RAG)**   
- ✅ **Download and process large datasets efficiently**   
- ✅ **Generate responses using an AI model**   
- ✅ **Analyze and visualize retrieval success** 
- ✅ **LLMs = AI that predicts words based on what it learned.**
- ✅ **RAG = AI + Search Engine (Finds new information before answering).**
- ✅ **HPC = Super powerful computers that make AI run much faster.**

🚀 **Next Workshop:** [🔍 Ethical AI & Future Trends](https://github.com/DrAlzahrani/HPC-AI-Resources/wiki/hpc-ethical-ai)  

### 🔗 Additional AI & HPC Resources 📚  

- [Project Jupyter Documentation](https://docs.jupyter.org/en/latest/)     
- [Python Introduction](https://www.w3schools.com/python/python_intro.asp)<br>
⚠ **Warning:** Please use only the two green buttons (“Previous” and “Next”) to navigate the tutorial. Avoid clicking on other links to prevent being redirected to ads.      
- [CSUSB: High-Performance Computing (HPC) Resources](https://www.csusb.edu/faculty-center-for-excellence/idat/high-performance-computing)   
- [AWS: What is Retrieval-Augmented Generation (RAG)?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)

🎉 Keep learning AI, and see you at the next workshop! 🚀
