# Emmanuel's P. A. I. R. (Personal AI Résumé)

This repository hosts Emmanuel's **Personal AI Resumé (P.A.I.R)**, an interactive chatbot that presents my career, projects, and skills in a dynamic way.  

It combines:  
- A **profile panel** with personal/professional details.  
- A **mini-chat app** where visitors can ask questions.  

---

## 🌐 Live Access

- **Chat App (GitHub Pages):**  
  👉 [https://emmanuelre8.github.io/EmmaBot_v1/](https://github.com/EmmanuelRE8/EVABot_v2))/)  

---

## 🎯 Purpose

The goal of P.A.I.R Bot is to go **beyond a traditional CV** and showcase my experience through an **interactive, AI-powered format**.  

Instead of just reading static text, recruiters and colleagues can:  
- **Ask questions** about my projects, skills, and impact.  
- Learn about my **career timeline, roles, and availability**.  
- Explore **STAR-style answers** to behavioural/soft skill questions.  
- See how the BI/AI tools I created can be applied to storytelling in real-world career fairs.  

---

## 🛠️ How It Was Built

1. **Frontend (GitHub Pages)**  
   - `index.html` → A responsive web app (HTML + CSS + Vanilla JS).  
   - Loads `profile.json` (basic info, availability, work history).  
   - Loads `kb.json` (projects, impact, tools, soft skills).  
   - Loads `star_bank.json` (STAR answers for soft skills).  
   - Provides a clean **chat interface** for interaction.  

2. **Backend (Cloudflare Workers)**  
   - A Worker (`src/index.js`) handles incoming chat requests.  
   - It detects intent:  
     - *Profile questions* → uses `profile.json`.  
     - *STAR/soft skill questions* → uses `star_bank.json`.  
     - *Project/impact questions* → uses `kb.json`.  
   - Calls **Groq API** (`llama-3.1-8b-instant`) via OpenAI-compatible endpoint.  
   - Returns concise, bullet-style answers.  
   - Uses CORS headers for public web access.  

3. **Data & Knowledge Base**  
   - `profile.json` → name, studies, experience, work history, preferences.  
   - `kb.json` → project portfolio, KPIs, actions, impacts, tools.  
   - `star_bank.json` → STAR responses (Situation, Task, Action, Result).  

4. **Deployment**  
   - Frontend → hosted free on **GitHub Pages**, accessible by QR code.  
   - Backend → deployed on **Cloudflare Workers** with environment secret `GROQ_API_KEY`.  
   - Integrated seamlessly: frontend sends chat queries to Worker, Worker calls Groq LLM + JSON sources, answers come back to the UI.  

---

## 📂 Repository Structure

- `index.html` → main interactive chatbot (profile panel + chat).  
- `onepager.html` → career one-pager (printable as PDF).  
- `profile.json` → personal info, availability, work history.  
- `kb.json` → projects and professional impact.  
- `star_bank.json` → soft skills (STAR examples).  
- `src/index.js` → Cloudflare Worker code.  

---

## 💡 Learning Outcomes

This project shows how to combine **BI, AI, and storytelling**:  
 
- Uses **LLMs** in a practical, low-cost way (Groq API).  
- Integrates **GitHub Pages + Cloudflare Workers** for free hosting.  
- Provides a **hands-on proof** of how BI professionals can make data **accessible and engaging**.  

---

👉 This README itself becomes part of the narrative: showing not only *what P.A.I.R. does*, but also *how it was engineered*.  
