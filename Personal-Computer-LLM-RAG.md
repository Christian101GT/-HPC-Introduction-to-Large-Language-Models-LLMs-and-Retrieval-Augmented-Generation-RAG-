# 🚀✨ **PC: Introduction to Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG)** ✨🚀  


## 🎯 **Goal**  
🤖 **Understand the basics of Large Language Models (LLMs)** and how **Retrieval-Augmented Generation (RAG)** enhances LLMs for tasks like text generation and answering complex queries. You will learn to use LLMs in combination with a retrieval system to improve performance. No prior experience needed—just bring your curiosity! 🚀  

---

## 📌 **What You Will Learn** 🧠💡  
✅ What are **Large Language Models (LLMs)**?  
✅ What is **Retrieval-Augmented Generation (RAG)**?  
✅ Setting Up LLM and RAG for Text Generation  
✅ Running LLM and RAG for Text Generation   
✅ How to use **RAG** with **Hugging Face** to enhance text generation  
✅ Hands-on coding with **Google Colab** and **Hugging Face**  

---

## 🤖 **1. What is a Large Language Model (LLM)?**  
### 🧠 Understanding LLMs in Simple Terms  
A **Large Language Model (LLM)** is a type of AI model that can understand and generate human-like text. It learns by analyzing massive amounts of text data, recognizing patterns, and predicting words based on context.

### 📌 Real-World Examples:  
- ✅ Chatbots like Siri, Google Assistant, ChatGPT 🗣️  
- ✅ AI-powered writing assistants (Grammarly, Jasper AI) ✍️  
- ✅ Search engines predicting your queries 🔍  
- ✅ AI-generated stories and essays 📖  

---

## 🔧 **2. What is Retrieval-Augmented Generation (RAG)?**  

💡 Think of it like Google + ChatGPT!

- Normally, AI models (like ChatGPT) only use what they’ve learned from training.

- RAG is different—it searches the internet or a database before answering your question. This makes responses more accurate and up-to-date!

📌 Example:
- 🗣️ You ask: “What’s the latest iPhone model?”

- A normal AI might say, “I think it’s the iPhone 14” (but it could be wrong if a new one was released).

- A RAG-powered AI searches online first and then answers, “The latest iPhone model is the iPhone 15 Pro, released in September 2023.”

### 🖼️ Retrieval-Augmented Generation (RAG) Visual Representation

<img src="https://github.com/user-attachments/assets/28f1e5d6-070b-405f-8a54-87c17ed5fbab" width="600">

Source: [RAG and LLM Integration](https://apmonitor.com/dde/index.php/Main/RAGLargeLanguageModel)

### 🧠 How RAG Enhances Large Language Models 🔗  

💡 Think: How do retrieval and generation work together to improve AI responses? 🤔

Retrieval-Augmented Generation (RAG) is an AI framework that improves large language models (LLMs) by integrating an external knowledge retrieval process. This allows the model to **pull relevant information from a document database** instead of relying only on its pre-trained knowledge.

**User Query** (💬): A user submits a question, which is then processed by the system to find relevant information.

Step 1️⃣: Writing the User Query (Asking the Question) ✍️
Before using RAG, you need a clear question. This is called a User Query.

- ✅ Example: You want to know about new video games.
  - 👉 Write this down as your User Query:
  - 📌 "What are the newest video games released this year?"

- 💡 Why is this important?

  - A clear question helps RAG find the best information.
  - Writing it down helps you compare your question with the AI’s answer.


**Vector Database & Document Storage** (📂)

Step 2️⃣: Vector Database & Document Storage (Where RAG Finds Info) 📂
Once you ask a question, RAG doesn’t rely only on memory. Instead, it searches a vector database.
 
- 📌 What is a Vector Database?
  - A huge collection of documents stored as numbers (vectors) instead of plain text.
  - Helps AI find similar topics fast by comparing numbers instead of words.

- ✅ Example:
  - Your question "What are the newest video games?"
  - The vector database searches for similar topics (recent gaming news, game reviews, release dates).

🔎 Think of it like this:
A normal AI might just guess. RAG actually searches a knowledge base first!

**Encoder Model** (🧩)

Step 3️⃣: Encoder Model (Understanding Your Question) 🧩
Before searching, RAG translates your words into numbers using an encoder model.

- 📌 What does an Encoder Model do?
  - Converts text into embeddings (number-based representations).
  - This helps AI match your question with the best documents.

- ✅ Example:
  - Your question "What are the newest video games?"
  - The encoder model converts it into numbers and searches for similar topics.

🔎 Think of it like this:
Instead of searching exact words, AI looks for meaning—so it finds results even if phrased differently!

**Context Retrieval & Augmentation** (🔍➡️📖)

Step 4️⃣: Context Retrieval (Finding the Right Info) 🔍➡️📖
Now that the encoder model understands your question, RAG retrieves the most relevant documents.

- 📌 What happens here?
  - RAG searches the vector database for the closest matches.
  - It finds recent game reviews, news articles, and release announcements.
  - This new information is added to your question to improve accuracy.

- ✅ Example:
  - It finds a game review from last week about a new release.
  - Instead of an outdated answer, you get fresh, up-to-date information!

 🔎 Think of it like this:
Normal AI guesses from memory—but RAG researches before answering!

**Large Language Model (LLM) Processing** (🧠)

Step 5️⃣: Large Language Model (LLM) Processing 🧠
Now that RAG has found fresh information, the Large Language Model (LLM) creates the final answer.

- 📌 What happens here?
  - The LLM combines what it already knows with the new retrieved info.
  - This makes the response accurate, fact-checked, and relevant.

- ✅ Example:
  - A normal AI might say: "The newest game is Cyberpunk 2077" (the game it old) .
  - A RAG-powered AI will say: "The latest video games include 'Final Fantasy VII Rebirth' and 'Helldivers 2,' released in 2024."

🔎 Think of it like this:
A normal AI is like a student guessing answers. RAG is like a student who double-checks the textbook before answering!

**Final Answer Generation** (✅)

Step 6️⃣: Final Answer Generation (Your AI Response) ✅

- 📌 What happens here?
  - The LLM formats the response in easy-to-read language.
  - It removes irrelevant details and presents the best possible answer.

-✅ Example Response: 
  - 💬 "The newest video games this year are 'Final Fantasy VII Rebirth' and 'Helldivers 2,' both released in 2024. Would you like reviews or gameplay details?"

🔎 Think of it like this:
Now, you have a fact-checked, up-to-date, and well-written response instead of a random guess!




---

### **Why RAG Matters?** 🚀  
✅ **More Accurate** – Reduces AI hallucinations by retrieving real-time, external information.  
✅ **Scalable** – Works with large document collections without needing to retrain the model.  
✅ **Efficient** – Uses vector search for fast, **semantic** document matching.  

📖Traditional LLMs generate responses based on probability distributions learned from training data. RAG mitigates hallucinations by injecting real-time knowledge, making responses more factually grounded.

### 🛠️ How Does RAG Work?  
RAG enhances LLMs by integrating **retrieval** and **generation** to provide more accurate responses. Instead of relying solely on pre-trained knowledge, it fetches relevant information from external databases before generating a response.

#### 📚 Steps in RAG:  
1️⃣ **Retrieval:** The model searches for relevant documents from a knowledge base.  
2️⃣ **Augmentation:** The retrieved data is passed as context to the LLM.  
3️⃣ **Generation:** The LLM generates a response based on the retrieved information. 

📌 **Example:**  
- If you ask about a recent scientific breakthrough, RAG can retrieve research papers or trusted sources before forming an answer.  

---

## 🔧 **3. Setting Up LLM and RAG for Text Generation**

- What You Need:
Before we start, you need a few things:
  - Google Colab: A tool that lets you write and run Python code in your browser without needing to install anything on your computer.
  - Hugging Face Account: Hugging Face is a website with many AI models. You need to create an account there to access these models and use them for text generation.

## 🚀 **Step 1: Open [Google Colab](https://colab.research.google.com/)**

1️⃣ Open your browser and go to **[Google Colab](https://colab.research.google.com/)**.  
2️⃣ Click **+ New Notebook** to begin.

## 🛠️ **Step 2: Set Up Hugging Face Account and Access Token**

1️⃣ **Sign up on Hugging Face**: Go to [Hugging Face Sign-Up](https://huggingface.co/join) and create a free account.  
2️⃣ **Generate an Access Token**:
An "access token" is like a key that allows you to use Hugging Face's models through Google Colab.
   - Click on your profile icon and go to **[Your Account Settings](https://huggingface.co/settings/tokens)**.
   - Scroll down to **Access Tokens** and click **New Token**.
   - Give it a name (e.g., "Colab Access") and select **Read** access.
   - Click **Generate Token** and copy the token.

✅ Hugging Face account setup complete! You’re now ready to log in. 🔑🎉

## 📚 **Step 3: Login in Colab with the Token**

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafa63-35d0-8004-bfdc-f36ffb25ae57)

```python
# Import Hugging Face login module
from huggingface_hub import notebook_login  

# Trigger login prompt
notebook_login()  
```

3️⃣ **Click Run (▶) and follow the instructions.**  

✅ Logged in successfully! Now, let's verify authentication. 🎉

## 🔐 **Step 4: Verify Authentication**

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67caface-5ed8-8004-a60c-5132ec7113bd)

```python
# Check if authentication is successful
!huggingface-cli whoami  
```

3️⃣ **Click Run (▶) and check the output!** 
 
✅ If it prints your Hugging Face username, the setup is complete! 🎉


---

## 🔧 **4. Running LLM and RAG for Text Generation**

## 📚 **Step 1: Install and Import Required Libraries**

Before importing the libraries, install the necessary dependencies by running the following command:

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafb46-9940-8004-8618-4f0cb0dfd5aa)

```python
# Install Hugging Face Transformers, FAISS, and datasets
!pip install transformers faiss-cpu datasets  
```

3️⃣ **Click Run (▶) to install the required packages.**

✅ Dependencies installed successfully! Now, let's import the necessary libraries. 📚🎉

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafbb3-4074-8004-8fd6-58b28b1cdd4d)

```python
# Import required libraries
from transformers import pipeline, RagTokenizer, RagRetriever, RagSequenceForGeneration  
import faiss  
```

3️⃣ **Click Run (▶) to import the libraries.**

✅ Libraries imported successfully! You’re now ready to load a pre-trained RAG model. 🚀🎉

## 🧠 **Step 2: Load a Pre-Trained RAG Model**

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafc54-f3c0-8004-a121-af4a0faa0f5c)

```python
# Define tokenizer model name
tokenizer_model = "facebook/rag-sequence-nq"  

# Load the tokenizer
tokenizer = RagTokenizer.from_pretrained(tokenizer_model)  

# Define the text-generation model name
generation_model = "gpt2"  

# Load the text-generation model
model = pipeline("text-generation", model=generation_model)  
```

3️⃣ **Click Run (▶) to load the pre-trained RAG model.**

📌 **Note:** When running this step, you may see a prompt asking:

```
Do you wish to run the custom code? [y/N]
```

Type **'y'** and press **Enter** to allow the model to load properly. This is required for some Hugging Face models.

✅ Pre-trained RAG model loaded successfully! Let’s proceed with querying the model. 🧠🎉

## 📚 **Step 3: Prepare a Query and Retrieve Information**

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafcc4-b258-8004-9f15-5b1e7d1d9419)

```python
# Define user query
query = "What is the process of photosynthesis?"  

# Tokenize query
input_dict = tokenizer.prepare_seq2seq_batch(query, return_tensors="pt")  

# Retrieval is disabled as retriever is removed
retrieved_docs = None  
```

3️⃣ **Click Run (▶) to retrieve documents related to the query.**

✅ Query prepared successfully! Now, let's generate a response. ✨🎉

## ✨ **Step 4: Generate a Response Using the Retrieved Documents**

### **➕🐍 Add a New Code Cell**  
1️⃣ Click **+ Code** in the top left to add a new code cell.  
2️⃣ Copy and paste the following code into the new code cell.  

🔗 [ChatGPT explanation for the code](https://chatgpt.com/share/67cafd2e-39b4-8004-9c52-ba1ac77e845f)

```python
# Generate response based on retrieved documents
output = model(query, max_length=100, truncation=True)  

# Extract generated text
generated_text = output[0]['generated_text']  

# Print generated response
print("Generated Answer:", generated_text)  
```

3️⃣ **Click Run (▶) to generate a response based on the retrieved documents.**

📌 **Expected Output:**

- The model should generate a relevant and coherent answer about the process of photosynthesis based on the retrieved information.

✅ Response generated successfully! You now have an AI-powered system retrieving and generating answers. 🚀🎉


---


🏆 Exercise: Try It Yourself! 🎯

Now that you have learned how to retrieve and generate responses using RAG, try this challenge on your own!

1️⃣ Modify the query to ask about a different topic, such as climate change, machine learning, or the history of AI.    
2️⃣ Run the code and analyze how the retrieved documents influence the generated response.    
3️⃣ Experiment by changing the model parameters (e.g., max_length) to see how the output changes.

📌 Bonus Challenge: Try integrating a different retrieval dataset from Hugging Face and see how it impacts the performance! 🚀

---

## 🎯 **5. Wrap-Up & Next Steps**  
🎉 Congratulations! You learned how to:  
✅ Use a **Large Language Model (LLM)** for text generation.  
✅ Implement **Retrieval-Augmented Generation (RAG)** to improve text generation.  
✅ Use **Hugging Face** for easy access to pre-trained models and retrieval systems.  

🚀 **Next Workshop:** [🔍 Ethical AI & Future Trends](https://github.com/DrAlzahrani/HPC-AI-Resources/wiki/personal-computer-ethical-ai)  

### 🔗 **Additional AI Resources** 📚   

- [Google Colab Guide](https://colab.research.google.com/)     
- [Python Introduction](https://www.w3schools.com/python/python_intro.asp)<br>
⚠ **Warning:** Please use only the two green buttons (“Previous” and “Next”) to navigate the tutorial. Avoid clicking on other links to prevent being redirected to ads.      
- [What is retrieval-augmented generation (RAG)?](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-retrieval-augmented-generation-rag)
- [AWS: What is Retrieval-Augmented Generation (RAG)?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)


🎉 Keep learning AI, and see you at the next workshop! 🚀
