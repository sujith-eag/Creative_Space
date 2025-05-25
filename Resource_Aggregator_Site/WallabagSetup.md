
You want to **self-host Wallabag**, a read-it-later app like Pocket, on your computer or server. There are two main ways to do that:

---

## Two Ways to Install Wallabag

### Option 1: **Using Docker** (Easy Mode – like using a pre-packaged Wallabag)

**What is Docker?**  
Docker is a tool that lets you run software (like Wallabag) in a "container" — a complete package that works the same on any machine.

**What you'll do:**

- Install Docker (once).
    
- Run a few copy-paste commands to start Wallabag.
    
- Open your browser and start using Wallabag.
    

---

### Option 2: **Manual Install** (Advanced – set up everything piece by piece)

**What this means:**

- You manually install everything Wallabag needs: PHP, a web server (like Nginx or Apache), a database (like PostgreSQL or MySQL), etc.
    
- You configure the app step-by-step.
    

This gives you more control but is more complex.

---

## Let’s Pick One: DOCKER METHOD (Easy & Fast)

### ✔ Step-by-Step (Docker)

#### 🔹 Step 1: Install Docker

**On Ubuntu/Debian:**

```bash
sudo apt update
sudo apt install docker.io
```

**On Mac/Windows:**  
Download Docker Desktop: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

---

#### 🔹 Step 2: Start Wallabag using Docker

Copy and paste this into your terminal:

```bash
docker volume create wallabag_data
docker volume create wallabag_images

docker run -d --name wallabag \
  -v wallabag_data:/var/www/wallabag/data \
  -v wallabag_images:/var/www/wallabag/web/assets/images \
  -p 7780:80 \
  wallabag/wallabag
```

This:

- Downloads the Wallabag app
    
- Starts it in a "container"
    
- Makes it available on your computer at port `7780`
    

---

#### 🔹 Step 3: Open Wallabag

In your browser, go to:

**[http://localhost:7780](http://localhost:7780)**

(If you're on a server, replace `localhost` with your server's IP.)

Create your account and you're done 🎉

---










You can host Wallabag for **free or very cheap** using several options — though free tiers often come with limitations (like storage, runtime hours, or sleep modes). Here's a breakdown of the **best free (or nearly free) server options** to host Wallabag:

---

## ✅ 1. **Railway** – Free container-based hosting

### 🔹 Pros:

- Docker support (easy for Wallabag)
    
- Free tier with 500 hours/month
    
- Simple UI and CLI
    

### 🔹 How to use:

- Sign up at [https://railway.app](https://railway.app)
    
- Create a new project → “Deploy from Repo” → use [https://github.com/wallabag/wallabag](https://github.com/wallabag/wallabag)
    
- Add a PostgreSQL or MySQL plugin (Wallabag needs a DB)
    
- Configure your `.env` variables
    
- Done!
    

**Limitation:** Apps may sleep after inactivity, unless upgraded.

---

## ✅ 2. **Render** – Easy free hosting with Docker support

### 🔹 Pros:

- Free tier with automatic HTTPS
    
- Supports Docker and web services
    

### 🔹 How to use:

- Go to [https://render.com](https://render.com)
    
- Sign up → "New Web Service"
    
- Connect to GitHub → use the Wallabag repo
    
- Set environment variables
    
- Add PostgreSQL database (free tier available)
    

**Limitation:** Sleep after inactivity on free plan.

---

## ✅ 3. **Fly.io** – Runs Docker apps globally

### 🔹 Pros:

- Docker-based
    
- Free tier includes 3 shared CPUs + 256MB RAM
    

### 🔹 How to use:

- Install the Fly CLI: `flyctl`
    
- Clone Wallabag repo
    
- Run `fly launch` in the repo folder
    
- Deploy it
    

🔗 [https://fly.io](https://fly.io)

---

## ✅ 4. **Glitch.com or Replit** – More for demos/testing

These are fun for lightweight apps, but Wallabag might be too resource-heavy for them long-term.

---

## ✅ 5. **Self-Host at Home (Free)**

If you're comfortable with your own hardware:

- Raspberry Pi, old laptop, or home server
    
- Install Docker + Wallabag
    
- Optional: use [Tailscale](https://tailscale.com/) or [ngrok](https://ngrok.com/) to access it from anywhere
    

---

## 🔒 Important Notes

- Always use **HTTPS** if exposing Wallabag publicly (some services handle this for you).
    
- Backup your database if you're storing articles long-term.
    
- Free services may have data/storage limits.
    

---

## 🚀 Recommendation for Beginners

|Platform|Best For|Notes|
|---|---|---|
|Railway|Easiest setup|UI + GitHub deploy|
|Render|Full-stack option|Similar to Heroku|
|Fly.io|Dev-friendly|CLI-based but powerful|
|Home server|Max control (free)|Needs port forwarding or Tailscale|

---


Yes — if you're **self-hosting Wallabag on your laptop**, then:

---

## ✅ Your laptop **must be ON and connected to the internet** whenever you want to:

1. **Save articles** (from phone, browser, etc.)
    
2. **Access and read saved articles** from other devices
    
3. **Sync with mobile apps** (if you're using them)
    

---

### 🔌 Why?

Your laptop is acting like a **server** — and for any server to work, it needs to be:

- Powered on
    
- Connected to the internet
    
- Running the Wallabag service
    

If your laptop is **off, asleep, or disconnected**, Wallabag will be **inaccessible** — from your phone, browser extensions, etc.

---

## 🧩 Workarounds & Tips

### 💡 1. **Just use Wallabag locally**

If you only save/read articles from that same laptop:

- No problem — just visit `http://localhost:7780`
    
- It works fine even offline, as long as Wallabag is running
    

---

### 💡 2. **Use Tailscale for remote access (no port forwarding)**

If you want to use Wallabag from your phone or another device **even when not at home**:

- [Install Tailscale](https://tailscale.com/) on your laptop and phone
    
- It creates a private secure network
    
- Access Wallabag from anywhere via a fixed internal address
    

No need to open ports or deal with firewalls.

---

### 💡 3. **Use ngrok to expose your laptop temporarily**

Want to share Wallabag over the web **without setting up a domain**?

- Install [ngrok](https://ngrok.com/)
    
- Run:
    
    ```bash
    ngrok http 7780
    ```
    
- It gives you a temporary web address like `https://abc123.ngrok.io`
    

Useful for short-term external access.

---

## 🔄 Alternative: Always-on Devices

If you want 24/7 access **without needing your laptop always on**, consider:

- A Raspberry Pi ($35–$50)
    
- A low-power mini-PC (Intel NUC, old laptop)
    
- A VPS (~$5/month) like DigitalOcean, Hetzner, Linode, etc.
    

---

Would you like help setting up Tailscale or ngrok so you can access Wallabag from your phone even when your laptop is at home?

