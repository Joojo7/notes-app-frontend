# 📝 Node Next Sample App

This is a simple sample frontend application built with **Next.js 15**, **React 19**, and **TailwindCSS 4**.
It’s designed for quick deployment to **Akamai Linode** as a dummy frontend, useful for testing cloud setups, subdomain routing, and reverse proxy configurations.

---

## 🚀 Features

- Next.js 15 with Turbopack support
- React 19
- TailwindCSS 4
- Simple JWT-based login and note-taking interface
- Suitable for reverse proxy via Apache/Nginx

---

## 📦 Prerequisites

Make sure you have the following installed on your server:

- **Node.js** (v18+ recommended)
- **npm** or **yarn**
- **Git** (for cloning)
- A **Linode instance** (Debian/Ubuntu preferred)
- Optional: Apache or Nginx if using reverse proxy setups

---

## 🛠️ Setup Instructions

1. **Clone the Repository**
  ```
   git clone https://github.com/your-username/node-next-sample.git
   cd node-next-sample
  ```

2. **Install Dependencies**

  ```
   npm install
  ```

3. **Start the Development Server**

  ```
   npm run dev
  ```

   > Visit: `http://localhost:3000`

4. **Build and Start for Production**

  ```
   npm run build
   npm start
  ```

   > App will run on `http://localhost:3000` by default.

---

## 🧱 Reverse Proxy (Optional)

If you're routing through Apache/Nginx, configure the reverse proxy to forward requests to port `3000`.
Example Apache snippet:

```
ProxyPass / http://localhost:3000/
ProxyPassReverse / http://localhost:3000/
```

---

## 🌐 Deployment on Akamai Linode

This app can be deployed on a Linode VPS as a containerized service or as a raw Node.js process. You can:

* Use **PM2** to keep it running
* Expose it behind a reverse proxy
* Bind it to your subdomain (e.g. `https://app.yourdomain.com`)

For full instructions, refer to your article’s deployment section.

---

## 📁 Project Structure

```
├── src/
├── public/
├── package.json
├── tailwind.config.js
└── README.md
```

---

## 📋 License

MIT — Feel free to use or extend as needed.
