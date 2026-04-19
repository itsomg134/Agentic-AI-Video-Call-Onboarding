# Agentic AI Video Call Onboarding

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Web Speech API](https://img.shields.io/badge/Web%20Speech-API-blue)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)
[![WebRTC](https://img.shields.io/badge/WebRTC-Supported-brightgreen)](https://webrtc.org/)

An intelligent, voice-driven onboarding system that simulates a human-like AI agent conducting a real-time video call. Built with vanilla HTML/CSS/JS and browser APIs — no backend required.

<img width="1881" height="971" alt="image" src="https://github.com/user-attachments/assets/07dae48e-9d31-44e7-af41-caec821481ea" />

##  Features

-  **Real Video Call Simulation** – Camera preview with mute/end controls
-  **Speech Recognition** – Speak naturally; the AI understands and responds
-  **Text-to-Speech** – AI "Sarah" speaks back with realistic voice
-  **Dynamic Conversation Tree** – AI adapts follow-ups based on your answers
-  **Sentiment Analysis** – Detects positive/neutral/negative keywords and adjusts tone
-  **Live Transcript** – Full conversation log with speaker labels
-  **Modern UI** – Glassmorphism design, animated avatar, responsive layout
-  **Privacy First** – All processing happens locally in your browser


##  How It Works

```
User speaks → Speech Recognition → Sentiment Analysis → 
Dynamic AI Response → Text-to-Speech → Avatar animates → 
Conversation continues
```

The AI agent maintains conversation state across 4+ onboarding steps:
1. **Ask Name** – Collect user identity
2. **Ask Role** – Understand department/position
3. **Ask Goal** – Identify primary objectives
4. **Ask Experience** – Gauge familiarity with AI tools
5. **Finalize** – Deliver personalized onboarding plan

##  Installation

### Option 1: Clone & Run Locally

```bash
git clone https://github.com/yourusername/agentic-ai-onboarding.git
cd agentic-ai-onboarding
# No build steps! Just open index.html
open index.html   # or double-click the file
```

### Option 2: One-Click Deploy

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/agentic-ai-onboarding)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/yourusername/agentic-ai-onboarding)

##  Usage Guide

1. **Allow Permissions** – Click "Enable Mic & Start Call" and grant camera/microphone access
2. **Speak Clearly** – Answer the AI's questions in natural language
3. **Watch the AI Respond** – Sarah will listen, process, and reply conversationally
4. **Follow the Flow** – Complete name → role → goal → experience steps
5. **End Call** – Click "End Call" when onboarding completes

### Controls

| Button | Action |
|--------|--------|
|  Enable Mic & Start Call | Initializes camera, mic, and starts conversation |
|  Mute Mic | Toggles microphone on/off during call |
|  End Call | Stops all media and ends session |

##  Conversation Examples

**User says:** *"I'm Alex, I'm a Product Manager"*  
**AI responds:** *"Wonderful! Product Manager is a key role. What's your primary goal with our platform?"*

**User says:** *"I'm excited to automate reports"* (positive sentiment)  
**AI responds:** *"Awesome to hear that energy! Nice to meet you, Alex! What is your role?"*

**User says:** *"I'm confused about the setup"* (negative sentiment)  
**AI responds:** *"I hear you, let's make this smooth. What would you like to achieve first?"*

##  Customization

### Modify Conversation Flow

Edit the `getAIResponse()` function in `index.html`:

```javascript
// Add new conversation steps
case 'ask_company_size':
    responseText = "How many people are in your team?";
    nextStep = 'ask_budget';
    break;
```

### Change AI Voice

```javascript
// In speakResponse() function
utterance.voice = speechSynthesis.getVoices().find(
    voice => voice.name === 'Google UK English Female'
);
utterance.rate = 0.9;  // Slower speech
utterance.pitch = 1.2; // Higher pitch
```

### Add Sentiment Keywords

```javascript
// In sentiment analysis section
if (lowerInput.includes('frustrated') || lowerInput.includes('stuck')) {
    state.sentiment = 'negative';
}
```

### Replace Avatar

Swap the SVG in `.avatar-circle` with an image:
```html
<img src="ai-avatar.gif" width="100" height="100" style="border-radius: 50%;">
```

##  Browser Support

| Browser | Speech Recognition | Text-to-Speech | Camera/Mic |
|---------|-------------------|----------------|------------|
| Chrome  |  Full             |  Full          |  Full      |
| Edge    |  Full             |  Full          |  Full      |
| Safari  |  Limited          |  Full          |  Full      |
| Firefox |  No               |  Full          |  Full      |


##  Project Structure

```
agentic-ai-onboarding/
├── index.html          # Complete application (HTML/CSS/JS)
├── README.md           # This file
└── LICENSE             # MIT License
```

##  Technical Architecture

- **Frontend**: Vanilla HTML5, CSS3 (Flexbox/Grid), ES6+
- **Media**: WebRTC (`getUserMedia`)
- **Speech Input**: Web Speech API (`SpeechRecognition`)
- **Speech Output**: Web Speech API (`SpeechSynthesis`)
- **State Management**: In-memory JavaScript object
- **No Dependencies** – Zero npm packages or external libraries

##  Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Improvements

- [ ] Add multilingual support (Spanish, French, German)
- [ ] Implement persistent conversation history (localStorage)
- [ ] Add emotion detection from facial expressions
- [ ] Integrate with GPT API for more natural conversations
- [ ] Add screen sharing for guided onboarding
- [ ] Create React/Vue component versions

##  License

Distributed under the MIT License. See `LICENSE` file for more information.

##  Acknowledgments

- [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) – For voice capabilities
- [WebRTC](https://webrtc.org/) – For real-time media
- [Font Awesome](https://fontawesome.com/) – Icon inspiration (icons via emoji)

##  Contact

Om Gedam

GitHub: [https://github.com/itsomg134](https://github.com/itsomg134)

Email: [omgedam123098@gmail.com](mailto:omgedam123098@gmail.com)

Twitter (X): [https://twitter.com/omgedam](https://twitter.com/omgedam)

LinkedIn: [https://linkedin.com/in/omgedam](https://linkedin.com/in/omgedam)

Portfolio: [https://ogworks.lovable.app](https://ogworks.lovable.app)
