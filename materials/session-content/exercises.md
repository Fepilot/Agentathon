# 🛠️ Hands-on Exercises

Practical exercises for Agentathon participants.

---

## 📋 Exercise Overview

| Exercise | Duration | Difficulty |
|----------|----------|------------|
| 1. Your First Agent | 30 min | Beginner |
| 2. Adding Knowledge | 45 min | Beginner |
| 3. Custom Topics | 30 min | Intermediate |
| 4. Adding Actions | 45 min | Intermediate |
| 5. Build Your Use Case | 3+ hours | Advanced |

---

## Exercise 1: Your First Agent

### Objective
Create a simple agent that can greet users and answer basic questions.

### Duration
30 minutes

### Steps

1. **Access Copilot Studio**
   - Navigate to [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com)
   - Sign in with your organizational account

2. **Create New Agent**
   - Click **Create** on the home page
   - Select **Start from scratch** or use a template
   - Name your agent: `My First Agent`
   - Click **Create**

3. **Configure Basic Settings**
   - Go to **Overview**
   - Add a description
   - Review the default instructions

4. **Test Your Agent**
   - Open the **Test** panel
   - Try greeting your agent
   - Ask a simple question

5. **Customize the Greeting**
   - Go to **Topics**
   - Find the **Greeting** topic
   - Modify the greeting message
   - Test again

### Success Criteria
- [ ] Agent responds to greetings
- [ ] Custom greeting message works
- [ ] Agent provides helpful fallback for unknown queries

---

## Exercise 2: Adding Knowledge

### Objective
Add knowledge sources so your agent can answer questions about specific topics.

### Duration
45 minutes

### Steps

1. **Prepare Knowledge Content**
   - Create a simple FAQ document or use the provided sample
   - Content should include:
     - Company information
     - Common questions
     - Process descriptions

2. **Add SharePoint Knowledge** (Option A)
   - Navigate to **Knowledge**
   - Click **+ Add knowledge**
   - Select **SharePoint**
   - Choose your SharePoint site
   - Select specific documents or sites
   - Click **Add**

3. **Add Website Knowledge** (Option B)
   - Navigate to **Knowledge**
   - Click **+ Add knowledge**
   - Select **Public website**
   - Enter the URL
   - Click **Add**

4. **Add File Knowledge** (Option C)
   - Navigate to **Knowledge**
   - Click **+ Add knowledge**
   - Select **Files**
   - Upload your document
   - Click **Add**

5. **Test Knowledge Retrieval**
   - Open the **Test** panel
   - Ask questions from your content
   - Verify accuracy of responses
   - Note any gaps

### Success Criteria
- [ ] Knowledge source successfully added
- [ ] Agent answers questions from knowledge
- [ ] Responses are accurate and relevant

---

## Exercise 3: Custom Topics

### Objective
Create custom topics to handle specific conversation scenarios.

### Duration
30 minutes

### Steps

1. **Identify a Scenario**
   - Example: Handling IT support requests
   - Define trigger phrases:
     - "I have a computer problem"
     - "My laptop is broken"
     - "IT help"

2. **Create New Topic**
   - Go to **Topics**
   - Click **+ Add a topic** > **From blank**
   - Name it: `IT Support Request`

3. **Add Triggers**
   - In the topic, add trigger phrases
   - Use variations to improve matching

4. **Build the Conversation Flow**
   - Add a **Message** node with greeting
   - Add a **Question** node to gather details
   - Store response in a variable
   - Add conditional logic if needed
   - End with appropriate action or message

5. **Test the Topic**
   - Open **Test** panel
   - Use trigger phrases
   - Complete the conversation flow
   - Verify variables are captured

### Example Flow

```
[Trigger: "I have a computer problem"]
     |
[Message: "I'm sorry to hear that! Let me help you."]
     |
[Question: "Can you describe the issue?"]
     |
[Store in: IssueDescription]
     |
[Question: "Is this urgent?"]
     |
[Condition: If urgent = Yes]
     |--- [Message: "I'll escalate this immediately."]
     |--- [Message: "I've logged your request."]
```

### Success Criteria
- [ ] Topic triggers correctly
- [ ] Conversation flows smoothly
- [ ] Variables capture user input
- [ ] Appropriate responses based on conditions

---

## Exercise 4: Adding Actions

### Objective
Enable your agent to perform actions using connectors and Power Automate.

### Duration
45 minutes

### Steps

1. **Understand Actions**
   - Actions allow agents to:
     - Retrieve data from systems
     - Create records
     - Send notifications
     - Trigger workflows

2. **Add a Pre-built Action**
   - Go to **Actions**
   - Click **+ Add an action**
   - Browse available connectors
   - Select a connector (e.g., SharePoint, Outlook)
   - Configure the action

3. **Create Power Automate Flow** (Advanced)
   - Go to **Actions**
   - Click **+ Add an action** > **Create a flow**
   - Build your automation
   - Save and test

4. **Use Action in Topic**
   - Open a topic
   - Add an **Action** node
   - Select your action
   - Map inputs from conversation variables
   - Handle outputs

5. **Test the Integration**
   - Trigger the topic
   - Verify action executes
   - Check outputs are displayed

### Example: Send Email Action

```
[User requests: "Send an email to my manager"]
     |
[Question: "What's the subject?"]
     |
[Question: "What's the message?"]
     |
[Action: Send Email via Outlook]
     |
[Message: "Email sent successfully!"]
```

### Success Criteria
- [ ] Action configured correctly
- [ ] Action executes from conversation
- [ ] Outputs handled appropriately
- [ ] Error handling in place

---

## Exercise 5: Build Your Use Case

### Objective
Build a complete agent for your identified use case.

### Duration
3+ hours (main Agentathon activity)

### Steps

1. **Review Your Design**
   - Reference your agent design document
   - Confirm knowledge sources available
   - List required actions

2. **Create Agent Structure**
   - Create new agent
   - Configure name and description
   - Set up system instructions

3. **Add Knowledge**
   - Connect all identified knowledge sources
   - Test knowledge retrieval

4. **Build Core Topics**
   - Create topics for main scenarios
   - Build conversation flows
   - Add variables and conditions

5. **Integrate Actions**
   - Add necessary actions
   - Connect to external systems
   - Handle responses and errors

6. **Test Thoroughly**
   - Test happy paths
   - Test edge cases
   - Test error scenarios
   - Gather feedback

7. **Refine and Improve**
   - Address issues found in testing
   - Improve responses
   - Add missing knowledge

8. **Prepare Demo**
   - Identify key scenarios to show
   - Prepare talking points
   - Practice the demo

### Deliverables
- [ ] Functional agent
- [ ] At least 3 working scenarios
- [ ] Knowledge source(s) connected
- [ ] At least 1 action integrated
- [ ] Demo-ready presentation

---

## 🎁 Bonus Challenges

### Challenge 1: Multi-language Support
Configure your agent to respond in multiple languages.

### Challenge 2: Sentiment Detection
Add logic to detect frustrated users and respond empathetically.

### Challenge 3: Handoff to Human
Implement escalation to a human agent for complex queries.

### Challenge 4: Analytics Dashboard
Set up custom analytics to track agent performance.

---

## 📝 Notes for Facilitators

- Circulate during exercises to provide support
- Have sample content ready for those who need it
- Encourage experimentation
- Celebrate progress, not just completion
