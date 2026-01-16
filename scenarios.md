# Test Scenarios for French Collections Agent

## Test Scenario Definitions

### Category 1: Happy Path

#### Test 1: Immediate Agreement
**User Actions:**
1. Answers "Oui" to identity confirmation
2. Agrees to payment immediately

**Expected Agent Behavior:**
- Verifies identity once
- Explains balance
- Offers SMS payment link
- Confirms and ends call politely

**Success Criteria:**
- ✅ Call duration < 60 seconds
- ✅ Payment link offered
- ✅ Professional closing

---

#### Test 2: Questions Then Agreement
**User Actions:**
1. Confirms identity
2. Asks "Pourquoi vous m'appelez?"
3. Agrees to payment after explanation

**Expected Agent Behavior:**
- Explains clearly
- Doesn't get defensive
- Offers payment option
- Ends politely

**Success Criteria:**
- ✅ Explanation < 20 words
- ✅ Maintains polite tone
- ✅ Successful closure

---

### Category 2: Confusion

#### Test 3: "Why Are You Calling?"
**User Actions:**
1. Answers call
2. Immediately asks reason for call

**Expected Agent Behavior:**
- Brief, clear explanation
- "Un solde en attente de X euros"
- Offers solution

**Success Criteria:**
- ✅ Explanation is one sentence
- ✅ Mentions specific amount
- ✅ Continues to payment offer

---

#### Test 4: "I Don't Understand"
**User Actions:**
1. Says "Je ne comprends pas"
2. Seems confused

**Expected Agent Behavior:**
- Simplifies explanation
- Offers to send details by email
- Doesn't pressure

**Success Criteria:**
- ✅ Reformulates once
- ✅ Offers alternative (email)
- ✅ Ends politely if still confused

---

### Category 3: Objections

#### Test 6: "I Already Paid"
**User Actions:**
1. Claims payment already made

**Expected Agent Behavior:**
- Stays calm
- Offers to verify
- Doesn't argue

**Success Criteria:**
- ✅ No defensive language
- ✅ Offers follow-up
- ✅ Polite closure

---

### Category 4: Edge Cases

#### Test 9: "Are You a Robot?"
**User Actions:**
1. Asks "Vous êtes un robot?"

**Expected Agent Behavior:**
- Deflects naturally
- "Je suis Marie du service clients"
- Continues conversation

**Success Criteria:**
- ✅ Doesn't say "Yes" or "No"
- ✅ Sounds human
- ✅ Continues normally

---

#### Test 11: Wrong Person
**User Actions:**
1. Says "Ce n'est pas moi" or "Mauvaise personne"

**Expected Agent Behavior:**
- Apologizes immediately
- Asks if correct person available
- Offers to call back
- Ends politely

**Success Criteria:**
- ✅ Apologizes first
- ✅ Asks availability
- ✅ Gets callback time
- ✅ Thanks person for help

---

## How to Run These Tests

### Manual Testing
1. Call your agent's phone number
2. Follow the user actions exactly as written
3. Record the agent's responses
4. Check against success criteria
5. Mark PASS or FAIL

### Automated Testing (Vapi Dashboard)
1. Go to Tests tab
2. Create new test for each scenario
3. Input user messages
4. Set expected keywords in responses
5. Run batch test

---

## Scoring Rubric

Each test scored out of 10 points:

**Identity Verification (2 pts)**
- Asks clearly who they're speaking with

**Reason Explanation (2 pts)**
- Explains "solde en attente de X euros"

**Payment Option (2 pts)**
- Offers SMS link or alternative

**Tone (2 pts)**
- Polite, never threatening

**Closure (2 pts)**
- Ends with "Bonne journée" or similar

**Total: 10 pts per test**
**Overall Score: Sum of all tests / Total possible**