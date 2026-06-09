# Deploy Your Portfolio in 10 Minutes

## What you're deploying
- `index.html` — your 3D space portfolio
- `api/chat.js` — serverless AI function (hides your API key)
- Vercel hosts everything for free

---

## Step 1 — Get your Anthropic API key (2 min)
1. Go to https://console.anthropic.com
2. Sign up (free)
3. Go to **API Keys** → **Create Key**
4. Copy it — looks like: `sk-ant-api03-...`
5. Add $5 of credits (lasts months for a portfolio chatbot)

---

## Step 2 — Push to GitHub (2 min)
```bash
# In your terminal, go to this folder:
cd "path/to/lokesh-portfolio"

git init
git add .
git commit -m "launch portfolio"

# Create a new repo on github.com, then:
git remote add origin https://github.com/YOUR_USERNAME/lokesh-portfolio.git
git push -u origin main
```

---

## Step 3 — Deploy on Vercel (3 min)
1. Go to https://vercel.com → **Add New Project**
2. Import your `lokesh-portfolio` GitHub repo
3. Click **Deploy** (leave all settings as default)

---

## Step 4 — Add your API key (1 min)
1. In Vercel, go to your project → **Settings** → **Environment Variables**
2. Add:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-ant-api03-...` (your key from Step 1)
3. Click **Save**
4. Go to **Deployments** → click the 3 dots on latest → **Redeploy**

---

## Done! 🚀
Your portfolio is live at `https://lokesh-portfolio.vercel.app` (or a custom domain).

The AI chat widget:
- Visitors click 🛸 to open the chat
- They ask questions about you
- Claude answers using everything in `api/chat.js`
- Click 🔊 to toggle voice on/off (it reads replies aloud)
- 4 suggestion chips for quick questions

---

## Custom domain (optional)
In Vercel → **Domains** → add `lokesh.dev` or `lokeshpullakandam.com` (~$12/year on Namecheap)

---

## Update your AI's knowledge
Edit `api/chat.js` → find the `SYSTEM_PROMPT` variable → update any details → push to GitHub → Vercel auto-redeploys.
