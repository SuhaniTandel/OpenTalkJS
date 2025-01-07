
# 🌟 JS Based Personal LLM 🌟

## 🛠️ Setup Instructions

### 1️⃣ Repository Cloning 
1. Open your terminal or command prompt 🖥️
2. Clone the repository using the command 🔗:  
   ```bash
   git clone https://github.com/SuhaniTandel/OpenTalkJS.git
   ```
3. Navigate into the project directory 📂:  
   ```bash
   cd OpenTalkJS
   ```
4. Open the project in your preferred code editor ✍️.

---

### 2️⃣ Dependencies Installation
1. Verify Node.js is installed by checking its version 🛠️:  
   ```bash
   node -v
   ```
   If Node.js is not installed, download and install it from [nodejs.org](https://nodejs.org).
   
2. Install the Ollama package 📦:  
   ```bash
   npm install ollama
   ```

3. Verify the installed version of Ollama 🔍:  
   ```bash
   ollama --version
   ```
   Ensure that Ollama is properly installed and running on your system.

---

### 3️⃣ Application Execution
1. Run the application using the command 🚦:  
   ```bash
   node main.js
   ```

2. View the Output 🎉:  
   The personal LLM will generate a response based on the prompt provided in the script.

---

### 📝 Example Script
Below is the example script provided in the project:

```javascript
import ollama from "ollama";

(async ()=>{
  try{
    const response = await ollama.chat({
      model: 'moondream:latest',
      messages: [{ role: 'user', content: 'Why is the sky blue?' }],
    })
    console.log(response.message.content)
  }catch(error){
    console.error("Error occurred:", error.message);
  }
})()
```

---

### 📜 Notes:
- Make sure the LLaMA 3.2 model is available in your local Ollama setup.
- The script generates a sample response for the prompt: *"Generate a marketing email."*
- Modify the `content` field in the script to test with different prompts.
