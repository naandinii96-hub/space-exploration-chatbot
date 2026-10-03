# 🚀 Space Research Chatbot

An AI-powered chatbot designed to answer questions about **space, astronomy, and space research** by combining a custom PDF knowledge base with live NASA information and AI-generated responses.

The project uses **Retrieval-Augmented Generation (RAG)** to retrieve relevant information from stored space-related documents and combines it with information from **NASA RSS feeds** before generating a response using **Groq**.

---

## 🌌 About the Project

The **Space Research Chatbot** is a project built to explore how **AI, RAG, vector databases, APIs, and web applications** can be combined to create a practical domain-specific AI assistant.

The chatbot can use:

* 📚 Space-related PDF documents as its knowledge base
* 🔎 Pinecone for storing and retrieving relevant information
* 🛰️ NASA RSS feeds for recent space-related information
* 🧠 Groq for AI-powered response generation
* 🎨 Streamlit for the chatbot interface

The backend was initially developed and tested using **Google Colab**, while the project files are maintained on **GitHub**.

---

## 🏗️ Project Architecture

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │    Streamlit    │
                  │    Frontend     │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │    Backend      │
                  │    Logic        │
                  └────────┬────────┘
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
      ┌─────────────────┐      ┌─────────────────┐
      │    Pinecone     │      │    NASA RSS     │
      │                 │      │                 │
      │ PDF Knowledge   │      │ Live Information│
      │     Base        │      │                 │
      └────────┬────────┘      └────────┬────────┘
               │                        │
               └────────────┬───────────┘
                            │
                            ▼
                   ┌─────────────────┐
                   │      Groq       │
                   │   AI Response   │
                   └────────┬────────┘
                            │
                            ▼
                   ┌─────────────────┐
                   │    Response     │
                   │    to User      │
                   └─────────────────┘
```

---

## 🔄 How It Works

### 1. 📄 PDF Knowledge Base

The chatbot uses space-related PDF documents as its custom knowledge source.

The documents are processed and stored in **Pinecone**, allowing the system to retrieve relevant information based on the user's question.

### 2. 🔎 Information Retrieval

When the user asks a question, the system searches the Pinecone vector database for relevant information from the uploaded documents.

This forms the **Retrieval-Augmented Generation (RAG)** part of the project.

### 3. 🛰️ NASA RSS Integration

The chatbot also uses **NASA RSS feeds** to access recent space-related information.

This provides an additional source of information alongside the static PDF knowledge base.

### 4. 🧠 AI Response Generation

The relevant retrieved information is provided to **Groq**, which generates the final natural-language response.

### 5. 🎨 Streamlit Interface

The chatbot is connected to a **Streamlit** frontend, providing an interactive interface where users can ask questions and receive AI-generated answers.

### 6. 🐙 GitHub

The project files are maintained in a **GitHub repository** for version control and project management.

### 7. ☁️ Future Deployment

The next step is to deploy the Streamlit application using **Streamlit Cloud** so that the chatbot can be accessed through a public web link.

---

## 🧰 Tech Stack

| Technology             | Purpose                                 |
| ---------------------- | --------------------------------------- |
| 🐍 **Python**          | Core programming language               |
| 📓 **Google Colab**    | Backend development and experimentation |
| 🔎 **Pinecone**        | Vector database and knowledge retrieval |
| 🛰️ **NASA RSS**       | Recent space-related information        |
| 🧠 **Groq**            | AI response generation                  |
| 🎨 **Streamlit**       | Frontend and chatbot interface          |
| 🐙 **GitHub**          | Version control and project files       |
| ☁️ **Streamlit Cloud** | Planned deployment platform             |

---

## ✨ Features

* 🚀 Space and astronomy focused AI chatbot
* 📚 Custom PDF knowledge base
* 🔎 Semantic information retrieval using Pinecone
* 🛰️ NASA RSS integration
* 🧠 AI-generated responses using Groq
* 💬 Interactive Streamlit interface
* 🔗 Combines static knowledge with recent information
* 🔐 API keys handled using environment variables
* 🐙 GitHub-based project management

---

## 🧠 What is RAG?

**Retrieval-Augmented Generation (RAG)** is an approach where an AI model retrieves relevant information from an external knowledge source before generating its answer.

In this project:

```text
User Question
      ↓
Search Pinecone
      ↓
Retrieve Relevant PDF Information
      ↓
Combine With NASA Information
      ↓
Send Context to Groq
      ↓
Generate Answer
```

This allows the chatbot to use information from the project's custom knowledge base instead of relying only on the language model's pre-existing knowledge.

---

## 📁 Project Structure

```text
space-research-chatbot/
│
├── app.py                  # Streamlit application
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
├── .gitignore              # Files excluded from GitHub
│
├── assets/                 # Images and other resources
│
└── ...
```

> The exact structure may vary depending on the final implementation.

---

## 🔐 Environment Variables

API keys should **never be uploaded to GitHub**.

Create a `.env` file locally and store your API credentials there.

Example:

```env
GROQ_API_KEY=your_groq_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

Make sure `.env` is included in your `.gitignore` file:

```text
.env
```

For the future Streamlit Cloud deployment, these credentials should be added through the platform's secrets/settings rather than being committed to the repository.

---

## 💻 Running the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/naandinii96-hub/space-research-chatbot.git
```

### 2. Open the project folder

```bash
cd space-research-chatbot
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API keys

Create a `.env` file and add the required API credentials.

### 5. Run the Streamlit application

```bash
streamlit run app.py
```

The Streamlit application should then open in your browser.

---

## 🚧 Project Status

### Current Status: In Development

The core chatbot has been developed and the project is currently being prepared for deployment.

### ✅ Completed

* [x] Backend development using Google Colab
* [x] PDF knowledge base
* [x] Pinecone integration
* [x] NASA RSS integration
* [x] Groq integration
* [x] Streamlit frontend
* [x] GitHub repository
* [x] Project documentation

### ⏳ Upcoming

* [ ] Deploy application using Streamlit Cloud
* [ ] Configure deployment secrets
* [ ] Test the publicly deployed application
* [ ] Add live demo link to this README

---

## ☁️ Deployment Plan

The application is **not deployed yet**.

The planned deployment workflow is:

```text
Google Colab
     ↓
Develop & Test Backend
     ↓
Streamlit Frontend
     ↓
GitHub Repository
     ↓
Streamlit Cloud
     ↓
Configure Secrets
     ↓
Deploy
     ↓
Public Web Application 🚀
```

Once deployment is complete, a **Live Demo** link will be added to this README.

---

## 🔮 Future Improvements

Some possible improvements for future versions include:

* 🌌 Add more space research papers and datasets
* 🛰️ Integrate additional NASA APIs
* 📡 Add more real-time astronomy data sources
* 🧠 Improve RAG retrieval and response accuracy
* 💬 Add conversation memory
* 📊 Add interactive space-data visualizations
* 🔭 Add astronomy image search
* 🎙️ Add voice-based interaction
* 🌍 Integrate information from other space agencies
* 📱 Improve the interface for mobile devices

---

## 🎯 Project Goals

This project was created to explore the practical implementation of:

* Artificial Intelligence
* Retrieval-Augmented Generation
* Large Language Models
* Vector Databases
* API Integration
* Prompt Engineering
* Streamlit Application Development
* Cloud Deployment
* GitHub and Version Control

The broader goal is to explore how **AI can be applied to space research and astronomy**.

---

## 👩‍💻 Author

**Nandini**

First-year B.Tech student exploring:

**AI/ML • Space Technology • Software Development • Research**

---

## 🚀 Built With Curiosity

> **Exploring space through the lens of AI.**

Built as a learning project to combine **AI + RAG + real-time information + space research** into one application.

⭐ More features and deployment coming soon!
