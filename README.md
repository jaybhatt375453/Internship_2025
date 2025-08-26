# 🌟 NextHire – AI-Powered Career Companion  

![NextHire Banner](https://img.shields.io/badge/NextHire-AI%20Career%20Companion-blueviolet?style=for-the-badge&logo=github)  

## 📑 Internship Report  
- **🎯 Title**: AI-Powered Career Companion (NextHire) – MERN + LLM Internship  
- **⏳ Duration**: 6 Weeks (Summer Internship 2025)  
- **👨‍🎓 Intern**: Jay Bhatt (22IT008)  
- **🏫 Institute**: CSPIT-IT  
- **💻 Mentor**: [Mentor Name / Organization if available]  
- **📂 Repository**: [GitHub Repo Link](https://github.com/jaybhatt375453)  
- **🔗 Live Demo**: [Project Deployment Link](https://next-hire-demo.vercel.app/)  

---

## 📌 Project Overview  
NextHire is an **AI-powered career companion** built using the **MERN stack** integrated with **Large Language Models (LLMs)**.  
It helps students and professionals with:  
- Resume building suggestions.  
- Interview preparation (Q&A with AI).  
- Skill-based career guidance.  
- Real-time job recommendations.  

The system leverages **MongoDB, Express.js, React.js, Node.js** and integrates **LLMs** through APIs for natural language interaction.  

---

# 📑 Internship Journey – Week by Week & Day by Day


```yml
weeks:
  - week: 1
    theme: "Getting Started – Setup & Planning"
    days:
      day1: "Introduction to internship, finalized project title & scope."
      day2: "Set up GitHub repo & local MERN environment."
      day3: "Installed dependencies (React, Node, MongoDB, TailwindCSS)."
      day4: "Studied project requirements, prepared architecture plan."
      day5: "Explored LLM APIs & feasibility for integration."
      day6: "Created initial README and documentation."
      day7: "Team sync & summary of week’s work."

  - week: 2
    theme: "Frontend Foundations"
    days:
      day1: "Built React project scaffold with Vite."
      day2: "Added Home Page with navigation (Login, Signup)."
      day3: "Designed UI using TailwindCSS + Material UI."
      day4: "Implemented reusable components (Navbar, Footer, Cards)."
      day5: "Setup routes with React Router."
      day6: "Basic state management with Context API."
      day7: "Weekly demo & code push to GitHub."

  - week: 3
    theme: "Backend Development & Database"
    days:
      day1: "Initialized Node.js + Express server."
      day2: "Setup MongoDB Atlas & tested CRUD operations."
      day3: "Created user schema & authentication model."
      day4: "Implemented JWT-based login/signup API."
      day5: "Connected frontend forms with backend APIs."
      day6: "Tested APIs using Postman."
      day7: "Code cleanup & documentation."

  - week: 4
    theme: "LLM & AI Integration"
    days:
      day1: "Explored OpenAI/LLM APIs for career suggestions."
      day2: "Built API wrapper for recommendation system."
      day3: "Integrated chatbot-like career Q&A."
      day4: "Tested career recommendation prompts."
      day5: "Connected frontend chat UI to backend LLM API."
      day6: "Optimized API calls & error handling."
      day7: "Weekly review + commit."

  - week: 5
    theme: "Enhancements & Deployment"
    days:
      day1: "UI polishing – improved dashboard design."
      day2: "Added progress tracker for user profile."
      day3: "Worked on resume analysis & job matching feature."
      day4: "Integrated LinkedIn API (basic fetch)."
      day5: "Prepared app for deployment."
      day6: "Deployed frontend on Vercel & backend on Render."
      day7: "Team review, testing on live environment."

  - week: 6
    theme: "Finalization & Reporting"
    days:
      day1: "Fixed minor bugs & improved UI responsiveness."
      day2: "Added error boundaries & loading states."
      day3: "Wrote detailed README + documentation."
      day4: "Prepared presentation slides."
      day5: "Conducted final testing with mentors."
      day6: "Submitted final report & blog."
      day7: "Internship presentation & wrap-up."


        
## ⚡ Key Features  
✅ User Authentication (Login/Signup with JWT & Google OAuth)  
✅ AI-Powered Resume Feedback  
✅ Interview Q&A Simulator (LLM-based)  
✅ Personalized Career Suggestions  
✅ Interactive Dashboard (React + Tailwind)  
✅ Backend API (Node.js + Express.js + MongoDB)  
✅ Deployment on Vercel / Render  

---

## 🛠️ Tech Stack  

**Frontend**: React.js, Tailwind CSS  
**Backend**: Node.js, Express.js  
**Database**: MongoDB Atlas  
**AI Integration**: OpenAI API (LLM integration)  
**Authentication**: JWT, Google OAuth 2.0  
**Deployment**: Vercel (Frontend), Render (Backend)  

---
results:
  - "Functional AI-powered dashboard."
  - "Resume feedback accuracy improved with prompt engineering."
  - "Users successfully tested Interview Q&A bot."
  - "Smooth integration between MERN stack + LLMs."

future_work:
  - "Add Job Scraping + AI Matching system."
  - "Implement Voice-based Interview Simulator."
  - "Add Multilingual Support for career guidance."
  - "Enhance UI/UX with analytics & progress tracking."

acknowledgments: >
  I sincerely thank my mentors, faculty members, and peers for their guidance 
  and support during this internship. Special thanks to OpenAI, MongoDB Atlas, 
  and Vercel for providing powerful tools to make this project possible.

references:
  - "MongoDB Documentation"
  - "React Documentation"
  - "Express.js Guide"
  - "OpenAI API Reference"
  - "TailwindCSS Docs"

author:
  name: "Jay Bhatt"
  portfolio: "https://jaybhatt375453.github.io"
  linkedin: "https://www.linkedin.com/in/jaybhatt375453/"
  github: "https://github.com/jaybhatt375453"


## 💻 Code Snippet (Sample AI API Call)  

```javascript
// Example: AI Resume Feedback API call
import express from "express";
import fetch from "node-fetch";
const router = express.Router();

router.post("/resume-feedback", async (req, res) => {
  const { resumeText } = req.body;
  try {
    const response = await fetch("https://api.openai.com/v1/chat/completions", {
      method: "POST",
      headers: {
        "Authorization": `Bearer ${process.env.OPENAI_API_KEY}`,
        "Content-Type": "application/json",
      },
      body: JSON.stringify({
        model: "gpt-4",
        messages: [{ role: "user", content: `Give feedback for this resume:\n${resumeText}` }],
      }),
    });
    const data = await response.json();
    res.json({ feedback: data.choices[0].message.content });
  } catch (error) {
    res.status(500).json({ error: "AI feedback failed" });
  }
});

export default router;
