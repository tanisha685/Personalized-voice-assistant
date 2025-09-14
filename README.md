
# Voice Assistant AI

A Python-based voice assistant powered by ElevenLabs Conversational AI. It can interact with users through speech or text, respond to prompts, and follow personalized schedules.

---

## Features

- Real-time conversation with a custom AI agent
- Text and audio interaction (speech recognition + audio output)
- Personalized user prompts and schedules
- Safe fallback to text if audio fails
- Easily configurable via `.env` file

---

## Demo

**Example Interaction:**

```

User: Hello!
Agent: Hello Tanisha, how can I help you today?

````

Audio input/output is supported if the agent is configured for speech.

---

## Tech Stack

- Python 3.13
- ElevenLabs API for conversational AI
- PyAudio for microphone input
- dotenv for environment variable management

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/tanisha685/Personalized-voice-assistant.git

````

2. Create a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate    # Linux/Mac
venv\Scripts\activate       # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root with your agent ID and API key:

```
AGENT_ID=your_agent_id_here
API_KEY=your_api_key_here
```

---

## Usage

Run the voice assistant:

```bash
python voice.py
```

* **If the agent supports audio:** Speak to the assistant; the conversation will be read aloud.
* **If audio fails or is not configured:** Interaction will fall back to text.

---

## Customization

* Change user name or schedule prompts in `voice.py`:

```python
user_name = "Tanisha"
general = "to talk to me"
```

* Modify `conversation_override` to set custom prompts or first messages.

---

## Troubleshooting

* **1002 Protocol Error / Segmentation Fault**

  * Make sure the agent supports speech input/output in ElevenLabs.
  * If audio is not needed, disable `DefaultAudioInterface()`:

```python
audio_interface=None
```

* **API key issues**

  * Ensure the key has `convai_write` permission.

---

