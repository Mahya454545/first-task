# 🧠 AI Tools Homework – Session 1

**Opofinance Internal AI Training Program**
Assigned by: Arash | Due: Report back in the group chat when done

---

## 🎯 Goal

Use an AI coding tool (Claude Code or Gemini CLI) to build a simple frontend dashboard — no backend, no database. Just HTML, CSS, and JavaScript. This is your first hands-on experience letting AI write real code for you.

---

## 🛠️ Step 1 — Set Up Your Tools

### Option A: Claude Code (Recommended)

1. Go to **claude.ai** and buy a **Pro plan** ($20/month) using your personal card
2. Download **Claude Code** (the CLI): https://claude.ai/code
3. Open your terminal and run:
   ```
   npm install -g @anthropic-ai/claude-code
   claude
   ```
4. Log in with your Anthropic account

### Option B: Gemini CLI (if you have a personal Gmail)

> Note: Gemini CLI works with a personal and work Google account (Gmail).

1. Make sure you have **Gemini Advanced** (Google One AI Premium) active on your personal Gmail
2. Install:
   ```
   npm install -g @google/gemini-cli
   gemini
   ```
3. Log in with your personal Gmail when prompted

---

## 💻 Step 2 — Create a GitHub Repository

1. Go to **github.com** and create a free account (if you don't have one)
2. Create a **new repository**:
   - Name it something like: `my-dashboard`
   - Set it to **Public**
   - Check "Add a README file"
3. Clone it to your computer:
   ```
   git clone https://github.com/YOUR_USERNAME/my-dashboard.git
   cd my-dashboard
   ```

---

## 🏗️ Step 3 — Build Your Dashboard with AI

Open your terminal inside the project folder and start Claude Code or Gemini CLI.

Then give it this prompt — **customize the role to match YOUR job**:

---

### 📋 Prompt Template (copy and edit this)

```
I want you to build a simple frontend-only dashboard for a [YOUR ROLE] at a forex brokerage.

Requirements:
- Pure HTML, CSS, and JavaScript — no backend, no database
- Two screens: Login page and Dashboard page
- Login page: email + password fields, a Login button, and a "Sign Up" link
- Sign Up page: name, email, password fields and a Register button
- After login (any credentials work, just simulate it with JS), show the Dashboard
- Dashboard should have: a sidebar with navigation links relevant to my role, a header with my name/avatar, and a main content area with 3–4 widgets or cards relevant to my work
- Make it look modern and professional

My role is: [DESCRIBE YOUR ROLE — e.g. "Support Agent who handles client tickets and account issues"]
```

**Replace the parts in [ ] with your actual role and details.**

Example usecases by teams:

- **Support Team** → client tickets, response time, open cases, escalations
- **Sales / IB** → leads, conversions, revenue, partner stats
- **Account Managers** → client portfolio, deposits, active accounts
- **Marketing** → campaigns, traffic, conversion rate, social stats
- **Finance / Back Office** → pending payouts, balances, transaction log

---

## 📤 Step 4 — Push to GitHub

Once your dashboard is ready:

```bash
git add .
git commit -m "Add my AI-built dashboard"
git push
```

---

## ✅ Step 5 — Report Back

Reply this post in the group:

1. 🔗 Your GitHub repo link
2. 📸 A screenshot of your dashboard
3. 💬 One sentence: _What surprised you most about working with the AI tool?_

---

## ❓ FAQ

**Q: I don't know how to code. Is that okay?**
A: Yes! That's the whole point. Let the AI write the code. You just describe what you want.

**Q: Can I use my Opofinance email for Claude Code?**
A: Yes — you sign up at claude.ai with any email and buy your own Pro subscription.

**Q: Can I use my Opofinance Google account for Gemini CLI?**
A: Yes — Gemini CLI requires a personal or work Gmail with Gemini Advanced. Use a personal account if you dont have a opofinance mail address (you might need to buy a subscription).

**Q: What if something doesn't work?**
A: Ask in the group! That's also part of the learning — figuring things out together.

---

_Good luck. There's no wrong answer here — just build something and share it._ 🚀
