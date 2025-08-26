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

internship_progress:
  week_1:
    title: "Project Setup & Research"
    days:
      day_1_2: "Research on Career Guidance systems & AI integration."
      day_3: "Environment setup (Node, React, MongoDB Atlas)."
      day_4_5: "GitHub repo setup & project planning."
      day_6: "Basic React frontend with landing page."

  week_2:
    title: "Authentication & Database"
    days:
      day_1_2: "Implement JWT-based authentication."
      day_3: "Google OAuth integration."
      day_4_5: "MongoDB schema design for users & resumes."
      day_6: "Connected backend with frontend login system."

  week_3:
    title: "AI Integration"
    days:
      day_1_2: "Integrated OpenAI API for Q&A."
      day_3_4: "AI-based Resume Feedback system."
      day_5_6: "AI Career Guidance chatbot implementation."

  week_4:
    title: "Frontend Enhancements"
    days:
      day_1_2: "Dashboard design with TailwindCSS."
      day_3: "Resume Upload & Feedback UI."
      day_4: "Interview Q&A frontend module."
      day_5_6: "Connected AI API with frontend components."

  week_5:
    title: "Testing & Deployment"
    days:
      day_1_2: "Unit & API testing with Postman."
      day_3: "Bug fixing in authentication & AI responses."
      day_4: "Backend deployed on Render."
      day_5_6: "Frontend deployed on Vercel."

  week_6:
    title: "Documentation & Final Report"
    days:
      day_1_2: "Created README & Documentation."
      day_3: "Final presentation preparation."
      day_4_5: "Writing Internship Report."
      day_6: "Submission & Review."

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
