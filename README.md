# 🤖 AI HR Evaluation Agent  
### End-to-End Intelligent Recruitment Automation System

---

## 🖼️ Project Overview
<img width="1503" height="544" alt="Workflow Overview" src="https://github.com/user-attachments/assets/f66d6e27-2f12-43df-8c11-1154297b722d" />

Brief:  
A complete recruitment process automation system combining **n8n**, **OpenAI**, and **Google Workspace** to handle intake, AI-driven evaluation, notifications, interview scheduling, and rejections — always keeping human validation in the loop.

---

## ✨ Quick Summary (The Essentials)
- Automatic CV evaluation using **GPT-4 Turbo**.  
- Structured record logging in **Google Sheets**.  
- Instant notifications to HR via **Telegram** and **Gmail**.  
- Automatic interview scheduling through **Google Calendar**.  
- **Human-supervised flow:** HR validates or overrides AI decisions.

---

## ✅ Key Features
- **Fully orchestrated pipeline** in **n8n (self-hosted)**.  
- **Human-in-the-loop:** every evaluation is reviewed by an HR technician.  
- **Traceability:** timestamps, scores, and status stored in Google Sheets.  
- **Scalable modular design:** independent agents (Evaluator, Scheduler, Reject).  
- **Deep integrations:** OpenAI, Google Docs, Sheets, Gmail, Calendar, Telegram.

---

## 🔁 Process Flow
1. Candidate submits a form with their CV (PDF).  
2. Text is automatically extracted from the CV.  
3. The corresponding job description is fetched from **Google Docs**.  
4. **OpenAI** compares the CV and JD, generating:  
   - Evaluation → *Apto / Pending / No Apto*  
   - Score → *0–10*  
   - Summary → *Short profile description*  
5. The result is logged into **Google Sheets**.  
6. **Telegram** notifies the HR technician with the summary and attached CV.  
7. HR validates:  
   - If **approved** → Scheduler Agent books interview in Calendar + sends email.  
   - If **rejected** → Reject Agent sends rejection email and updates the sheet.

---

## 🧱 Architecture & Stack
- **Automation Platform:** n8n (self-hosted)  
- **AI Engine:** OpenAI GPT-4 Turbo  
- **Documents Source:** Google Docs  
- **Database / Storage:** Google Sheets  
- **Calendar Integration:** Google Calendar  
- **Email System:** Gmail API  
- **Notifications:** Telegram Bot API  
- **Languages:** English / Spanish  

---

## ⚙️ Main Components
- **Candidate Intake (Form Trigger):** collects name, email, position, and CV (PDF).  
- **AI HR Evaluation Agent:** extracts, compares, scores, and summarizes.  
- **Human Validation:** via Telegram and Google Sheets review.  
- **Scheduler Agent:** finds free slot (Mon–Fri, 09:00–18:00), creates Meet link, sends Gmail invite.  
- **Reject Agent:** sends professional rejection email and updates Google Sheets record.

---

## 🚀 Quick Deployment
1. Import the JSON workflow into your **n8n** instance.  
2. Configure credentials for:  
   - Google Workspace (Docs, Sheets, Gmail, Calendar)  
   - OpenAI API Key  
   - Telegram Bot Token  
3. Connect the form submission node as the trigger.  
4. Run a test submission with a sample PDF CV and verify results in Google Sheets and Telegram.

---

## 🧾 Example Outputs
**Telegram Notification:**  
- **ID:** 3041  
- **Name:** John Doe  
- **Position:** AI Engineer  
- **Email:** john.doe@example.com  
- **Evaluation:** Apto  
- **Score:** 8.7  
- **Summary:** Strong automation and ML deployment background.  

**Google Sheets Entry:**  
| Date | Name | Email | Position | Evaluation | Score | Profile Summary | Status |
|------|------|--------|-----------|-------------|------:|-----------------|---------|
| 19-10-2025 13:12 | John Doe | john.doe@example.com | AI Engineer | Apto | 8.7 | Automation and AI expertise... | Pending HR Review |

---

## 🖼️ Visuals
<img width="675" height="732" alt="Captura de pantalla 2025-10-19 185819" src="https://github.com/user-attachments/assets/6a8c52c9-81fa-40fc-91e8-12366d329836" />
<img width="502" height="521" alt="image" src="https://github.com/user-attachments/assets/a5337d9f-89c9-4f48-bed9-ef0c02e9002f" />



---

## 🧭 Author & Contact
Diego Pérez — AI Automation Specialist  
- 🔗 [LinkedIn – Diego Pérez García](https://www.linkedin.com/in/diego-perez-garcia)  
- 📧 diegoperezgarc@gmail.com  
- 📁 https://github.com/diegoperezg7/AI-Driven-HR-Evaluation-Agent

