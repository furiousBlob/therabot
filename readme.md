# TheraBot - Mental Health Chatbot

TheraBot is an AI-powered mental health support chatbot that provides emotional support, monitors user well-being, and maintains communication with healthcare providers. Built with Python and Streamlit, it offers a secure and empathetic platform for mental health conversations.

## Features

- **Intelligent Conversations**: Uses LLaMA 3.2 model for empathetic and context-aware responses
- **Real-time Emergency Detection**: Monitors conversations for signs of crisis and triggers immediate response
- **Healthcare Provider Integration**: Automatically sends session summaries to designated healthcare providers
- **Voice Response**: Converts text responses to speech for accessibility
- **Secure Data Management**: Maintains conversation history and user preferences securely
- **RAG (Retrieval Augmented Generation)**: Utilizes ChromaDB for enhanced response accuracy
- **SOS Alert System**: Emergency contact notification system with email integration

## Prerequisites

- Python 3.10
- Ollama with LLaMA 3.2 model
- ChromaDB
- Streamlit
- Gmail account (for email notifications)

## Installation

1. Clone the repository:
```bash
git clone [git@github.com:furiousBlob/therabot.git]
cd therabot
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Set up environment variables in `.env` file:
```
OPENAI_API_KEY=your_api_key
EMAIL_PASSWORD=your_email_password
```

## Project Structure

```
therabot/
├── pipeline/
│   ├── Data/
│   │   └── All/          # Training data and reference materials
│   ├── confidential/     # Secure credentials
│   ├── memory/          # Conversation memory storage
│   ├── onboarding-details/ # User and healthcare provider information
│   ├── therapist-specific-activities/ # Therapeutic activities
│   └── chromadb/        # Vector database storage
├── requirements.txt     # Project dependencies
└── README.md           # Project documentation
```

## Setup and Configuration

1. **Ollama Setup**:
   - Install Ollama and download the LLaMA 3.2 model
   - Ensure Ollama is running

2. **ChromaDB Configuration**:
   - Database will be automatically initialized on first run
   - Stores document embeddings for enhanced responses

3. **Email Configuration**:
   - Configure Gmail SMTP settings in the code
   - Enable "Less secure app access" or use App Passwords

4. **Emergency Contact Setup**:
   - Add emergency contact details during onboarding
   - Configure email settings for emergency notifications

## Usage

1. Start the application:
```bash
streamlit run app.py
```

2. Navigate through the sidebar options:
   - **Home**: Welcome page and resources
   - **Onboarding**: Set up user profile and preferences
   - **Chat**: Start conversation with TheraBot
   - **End Chat**: Conclude session and send summary to healthcare provider
   - **Delete Chat History**: Clear conversation history

## Security Features

- Secure credential storage
- Encrypted communication
- Protected user data
- Session management
- Secure database operations

## Emergency Response System

Current Implementation:
- Monitors conversations for crisis indicators including:
  - Suicidal ideation
  - Self-harm indicators
  - Crisis keywords
  - Emergency patterns
- When triggered:
  1. Sends immediate email notification to emergency contact
  2. Delivers conversation summary to healthcare provider
  3. Provides crisis resources to user

## Future Work

1. **Enhanced Emergency Response**:
   - Implementation of Twilio integration for emergency voice calls
   - SMS notifications for emergency contacts
   - Multi-channel alert system

2. **Planned Improvements**:
   - Real-time healthcare provider notifications
   - Integration with emergency services
   - Advanced crisis detection algorithms
   - Multiple emergency contact support

## Support

For support, please contact [prathusapkota3@gmail.com]

---
Created with ❤️ for mental health support
