# French Voice Collections Agent

A respectful French-language voice agent for debt collection, built in 2 hours using Vapi.ai.

## 🚀 Quick Start

### Demo Access

**Option 1: Call the Agent (Recommended)**
```
Phone: +1 (507) 702 4143
```


**Option 2: Web Demo**
```
[https://vapi.ai/demo/your-demo-link](https://www.loom.com/share/8ae1459db8a9451586336e28962473fe)
```


## 📋 What This Agent Does

✅ Conducts polite debt collection calls in French  
✅ Verifies caller identity respectfully  
✅ Explains outstanding balance clearly  
✅ Offers secure SMS payment link  
✅ Handles objections professionally  
✅ Never threatens or pressures  

---

## 🏗️ Architecture

**Platform:** Vapi.ai (No-code voice AI)  
**Language Model:** GPT-4  
**Voice:** ElevenLabs Charlotte (French)  
**Average Response Time:** 1.2 seconds  
**Call Duration:** 30-90 seconds  

---

## ⚙️ How to Run This Agent

### Prerequisites
- Vapi.ai account (free trial available)
- No coding required
- No installations needed

### Setup Steps (5 minutes)

1. **Sign up for Vapi**
```
   Visit: https://vapi.ai
   Create free account
```

2. **Import Agent Configuration**
   - Go to Dashboard → Create Assistant
   - Name: "French Collections Agent"
   - Copy prompt from `config/amazon.json`
   - Paste into "Instructions" field
   - Select Voice: "Charlotte (French)"
   - Save

3. **Get Phone Number (Optional)**
```
   Dashboard → Phone Numbers → Buy Number
   Select: France (+33)
   Assign to: French Collections Agent
```

4. **Test Immediately**
   - Call the number OR
   - Use web demo link

**Total setup time: < 5 minutes**

---

## 🧪 Running Self-Tests

### Automated Tests (Via Vapi Dashboard)

1. Go to **Tests** tab
2. Import test scenarios from `tests/scenarios.md`
3. Click **"Run All Tests"**
4. View results in dashboard

### Manual Testing

Call your agent and test these scenarios:

1. **Happy Path** - Agree to pay
2. **Confusion** - Ask "Why are you calling?"
3. **Wrong Person** - Say "This isn't me"
4. **Robot Question** - Ask "Are you a robot?"
5. **Angry Caller** - Show frustration

See `test-report.md` for detailed results.

---

## 🎨 Client Presets

Change the agent's tone for different brands:

### Amazon (Friendly & Solution-Focused)
```json
{
  "client_name": "Amazon Business",
  "tone": "friendly",
  "opening": "Bonjour, je suis Marie de Amazon Business."
}
```

### Dell (Professional & Technical)
```json
{
  "client_name": "Dell Technologies",
  "tone": "professional",
  "opening": "Bonjour, je suis Marie de Dell Technologies."
}
```

### Microsoft (Formal & Corporate)
```json
{
  "client_name": "Microsoft France",
  "tone": "formal",
  "opening": "Bonjour, je suis Marie de Microsoft France."
}
```

### How to Change Presets

1. Open `config/[client].json`
2. Edit the `client_name` and `tone` fields
3. In Vapi Dashboard:
   - Go to your Assistant
   - Replace `[CLIENT_NAME]` in prompt with new value
   - Save
4. Test immediately - tone will change!

**No code changes needed. Just edit JSON and update prompt.**

---

## 🔐 Environment Variables

If deploying via Vapi API (advanced users):
```bash
VAPI_API_KEY=your_vapi_api_key_here
PHONE_NUMBER=+33XXXXXXXXX
ASSISTANT_ID=your_assistant_id
```

**⚠️ Never commit API keys to this repository**

For no-code setup (this demo), no environment variables needed.

---

## 📊 Test Results

See **test-report.md** for:
- Success rates per scenario
- Response time analysis
- Failure modes
- Example transcripts

**Quick Summary:**
- Total Tests: 12
- Success Rate: 87%
- Avg Response Time: 1.2s
- P95 Response Time: 2.1s

---

## 📁 Project Structure
```
.
├── README.md              # This file
├── test-report.md         # Detailed test results
├── config/
│   ├── amazon.json        # Amazon Business preset
│   ├── dell.json          # Dell Technologies preset
│   └── microsoft.json     # Microsoft France preset
└── tests/
    └── scenarios.md       # Test case descriptions
```

---

## 🎥 Demo Video

**Loom Recording:** (https://www.loom.com/share/8ae1459db8a9451586336e28962473fe)

Shows:
- 2 live test calls in French
- Handling "Are you a robot?" question
- Handling wrong person scenario
- Test report walkthrough

---

## ⏱️ Build Time

**Total Time:** 1 hour 45 minutes

Breakdown:
- Agent design & prompt: 30 min
- Vapi setup & testing: 45 min
- Documentation: 20 min
- Video recording: 10 min

---

## 🔄 Production Deployment

This is a working prototype. For production:

**Recommended Stack:**
- Vapi.ai ($45/month unlimited)
- Or: Twilio + OpenAI ($20-30/month)
- Add: Call recording storage
- Add: CRM integration
- Add: Real-time monitoring dashboard

**Deployment timeline:** 1 business day

---


## 📜 License

This is a technical assessment project. Code and configurations are provided as-is for evaluation purposes.

---

## 🙏 Acknowledgments

Built with:
- [Vapi.ai](https://vapi.ai) - Voice AI platform
- [ElevenLabs](https://elevenlabs.io) - French voice synthesis

- [OpenAI GPT-4](https://openai.com) - Conversation logic
