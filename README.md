## 🌸 FrameSort Macro Bot - n8n Workflow 🌸
*A cute lil' AI Assistant for the FrameSort Addon Discord*


Welcome to the official n8n workflow behind the **FrameSort Macro Bot** - a Discord bot that helps players build World of Warcraft macros using FrameSort's dynamic variables. It reads the user's question, checks the FrameSort Macro Guide and the FrameSort Macro lua code, and then replies with clean, simplified macro suggestions. 

Think of it as a **Macro Generator Bot** that never sleeps. 

---

## ⭐ What This Bot Does ⭐

The FrameSort Macro Bot:
- **Monitors Mentions** in the `#macro-bot-channel`
- **Reads the user's question**
- **Fetches the FrameSort Lua Code** from Raw Github
- **Uses ChatGPT (gpt-5-chat-latest)** to generate a macro answer
- **Simplifies the macro using FrameSort's multi-variable rules**
- **Refuses to answer anything NOT related to FrameSort**
- **Redirects wrong-channel usage** to avoid spam

Basically: Someone can ask, How do i sheep a healer, and this bot spits out the macro in the proper format. 

---
## 🎓 Features Breakdown 🎓

### **1. Discord Trigger (#macro-bot-channel)**
Listens for bot mentions inside of the designated text channel.
and starts the macro help process.
*Discord trigger is not natively part of n8n, however is in a community node you will have to download first.*

### **2. HTTP Request**
Fetches the latest Parser.lua from the FrameSort Github repo so the bot always uses the most current macro logic.

### **3. LLM Chain**
Sends the user question + parser code + macro guide to the model with strict rules:
- Stay on topic
- Use FrameSort Variables
- Explain macros simply
- Never Answer unrelated questions

### **4. ChatGPT Node**
Powered by `GPT 5` using openai API key. 


### **4. Discord Reply**
Replies directly in the macro channel, tagging the user and giving a clean simplified macro answer.

### **6. Wrong Channel Handler**
If someone mentions the bot in `#general`, it send a cute redirect message instead of spamming anyone.


---

## How to Import into n8n

1. Open **n8n**
2. Go to **Workflows**
3. Click **Import**
4. Upload `FrameSort AI Bot.json`
5. Add your:
   - Discord Bot API credentials  
   - Discord Trigger credentials  
   - OpenAI API key  

And boom — you're live. 💅✨

---

## Why This Bot Exists

The FrameSort community constantly asks for macro help, so this bot:

- Gives consistent, correct answers  
- Teaches good macro-building habits  
- Relies on official docs + parser logic  
- Keeps the Discord clean  

And yes… it’s also cute. And we love that.

---

##  Credits

- **Verz** FrameSort Addon Creator   
- **Sophia** for building this whole iconic workflow  

