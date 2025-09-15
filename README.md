
conversation-management-groq/
│
├── Managing_Conversation_History_with_Summarization.ipynb  # Task 1 Notebook
├── JSON_Schema_Classification_&_Information_Extraction.ipynb # Task 2 Notebook
├── README.md                             # Main Documentation

# Conversation Management & Classification using Groq API

This repository implements two core tasks using the **Groq API (OpenAI SDK compatible)**:
1. **Conversation Management with Summarization**
2. **JSON Schema Classification & Information Extraction**

The project is implemented in **Google Colab Notebooks** (two separate files for each task) and version-tracked in GitHub.

---

## 📌 Task 1: Conversation Management with Summarization
**File:** `Managing_Conversation_History_with_Summarization.ipynb`

### Features
- Maintains running conversation history of user–assistant messages.
- Supports truncation:
  - By number of turns (last *n* messages).
  - By character length (max *k* characters).
- Periodic summarization:
  - Every *k-th run* of the conversation.
  - Summary replaces old history.
- Summarization powered by Groq models.

### Example Output
```json
[
  {
    "role": "user",
    "content": "Hi, I need help planning a Goa trip."
  },
  {
    "role": "assistant",
    "content": "Sure, what dates and budget?"
  },
  {
    "role": "user",
    "content": "Second week of October, budget 20k INR."
  },
  {
    "role": "assistant",
    "content": "Do you prefer hotels or homestays?"
  },
  {
    "role": "user",
    "content": "Hotels, beach-facing."
  }
]
...
    "role": "assistant",
    "content": "Okay, I'll suggest some options."
  }
]
````


## 📌 Task 2: JSON Schema Classification & Extraction

**File:** `JSON_Schema_Classification_&_Information_Extraction.ipynb`

### Features

* Defines a JSON schema to extract:

  * Name
  * Email
  * Phone
  * Location
  * Age
* Uses **Groq function calling (OpenAI-compatible)** for structured JSON outputs.
* Includes regex fallback for parsing if needed.
* Demonstrates parsing of 3 sample chats.

### Example Output

```json
[
  {
    "name": "Rahul Sharma",
    "email": "rahul25@gmail.com",
    "phone": "9876543210",
    "age": 25,
    "location": "Mumbai"
  },
  {
    "name": "Unknown",
    "email": "ananya30@yahoo.com",
    "phone": "9123456789",
    "age": 30,
    "location": "Delhi"
  },
  {
    "name": "Rohan Mehta",
    "email": "rohan.mehta@outlook.com",
    "phone": "9988776655",
    "age": 28,
    "location": "Bangalore"
  }
]
```

---

## ⚙️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/SAditya411/conversation-management-groq.git
cd conversation-management-groq
```

### 2. Install Dependencies

```bash
pip install groq openai
```

### 3. Configure API Key

```python
import os
os.environ["GROQ_API_KEY"] = "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 "
```

### 4. Run in Colab

* Open `Managing_Conversation_History_with_Summarization.ipynb` → Run cells for conversation history + summarization.
* Open `JSON_Schema_Classification_&_Information_Extraction.ipynb` → Run cells for JSON classification & extraction.


## ✅ Evaluation Mapping

* Task 1: Conversation management, truncation, periodic summarization.
* Task 2: JSON schema classification + structured outputs.
* Both tasks implemented separately.
* No frameworks used.
* Clear outputs + documentation.
* Google Colab & GitHub ready.

```

