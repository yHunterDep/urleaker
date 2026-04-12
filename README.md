<h1 align="center">🔍 URLeaker</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/yHunterDep/urleaker/main/urleaker.png" width="300"/>
</p>

<p align="center">
  <b>A powerful secret scanner for HTTP responses</b><br>
  API Keys • Tokens • Credentials • Misconfigurations • Recon
</p>

<p align="center">
  <a href="https://github.com/yHunterDep/urleaker">
    <img src="https://img.shields.io/badge/status-active-brightgreen?style=for-the-badge">
  </a>
  <a href="https://github.com/yHunterDep/urleaker">
    <img src="https://img.shields.io/badge/version-0.2.2-blue?style=for-the-badge">
  </a>
  <a href="https://www.python.org/">
    <img src="https://img.shields.io/badge/python-3.x-purple?style=for-the-badge">
  </a>
</p>

---

## 💻 Terminal Preview

<pre style="background-color:#000000;color:#ffffff;padding:16px;border-radius:8px;overflow-x:auto;">
$ ./urleaker -h

usage: urleaker [-h] -f FILE [-sv SEVERITY] [-api] [-t] [-cr] [-g] [-html] [-st] [-dc]
                [-c CONCURRENT] [-s] [-nc] [-v]

URLeaker 0.2.2 - By HunterDep ^^

options:
  -h, --help            show this help message and exit
  -f, --file FILE       Put file to scan. Ex: -f urls-js.txt
  -sv, --severity SEVERITY
                        Choice severities to scan (-sv unknown,low,medium,high,critical)
  -api, --api           Find APIKeys (Google, AWS, Firebase, etc)
  -t, --tokens          Find Tokens (Discord, Slack, Github, etc)
  -cr, --credentials    Find Credentials (Email, passowrds, etc)
  -g, --generic         Find generic API Key
  -html, --html         Find intersting object html
  -st, --social_takeover
                        Find social media profiles for potential takeover (Instagram, TikTok,
                        X, LinkedIn, YouTube)
  -dc, --dep_confusion  Find possible dependency confusion targets
  -c, --concurrent CONCURRENT
                        Number of concurrent threads (default: 20)
  -s, --silent          Skip banner mode
  -nc, --no_color       Remove colors from output
  -v, --verbose         Enable verbose output (detailed matches and additional context)

$ █
</pre>

---

## ⚙️ Installation

```bash
git clone https://github.com/yHunterDep/urleaker
cd urleaker
chmod +x urleaker
```

---

## 🚀 Usage

```bash
./urleaker -f urls.txt
```

---

## 🔥 Examples

```bash
./urleaker -f urls.txt
```

```bash
./urleaker -f urls.txt -api -t
```

```bash
./urleaker -f urls.txt -cr
```

```bash
./urleaker -f urls.txt -sv high,critical
```

```bash
./urleaker -f urls.txt -dc
```

```bash
./urleaker -f urls.txt -st
```

```bash
./urleaker -f urls.txt -v
```

```bash
./urleaker -f urls.txt -c 50
```

---

## 🧠 Features

- 🌐 Scan **any HTTP response body**
- 🔑 API key detection (AWS, Google, Stripe, Azure, etc)
- 🔐 Token leaks (Discord, GitHub, Slack, JWT, OAuth)
- 📧 Credentials (emails, passwords, FTP leaks)
- 🔒 Private keys & sensitive secrets
- 🧩 Generic secrets & environment variables
- 🧠 Dependency confusion detection
- 🌍 Social media takeover discovery
- ⚡ Multithreaded scanning
- 🎯 Severity filtering system
- 🧾 Verbose mode for deep analysis

---

## 🆕 What's New (v0.2.2)

- ➕ Added **dependency confusion detection** (`-dc`)
- ➕ Added **social takeover module** (`-st`)
- ➕ Added **verbose mode** (`-v`)
- ➕ Improved AWS/Azure detection regex
- ➕ Better output handling & stability
- ➕ Cleaner CLI structure
- ➕ More patterns and coverage

---

## 📂 Input Format

```txt
https://example.com/app.js
https://target.com/api
https://site.com/index.html
```

---

## 📤 Example Output

```bash
[AWS_SECRET_KEY] (critical) [https://target.com/api] [AMAZON_SECRET_KEY=agF...]

[FACEBOOK_ACCESS_TOKEN] (high) [https://target.com/modules/path/dom.php] [EAACE
..]

[DISCORD_TOKEN] (critical) [https://target.com/script.js] [MTIzNDU2...]

[EMAIL] (info) [https://target.com/page] [admin@example.com]

[WEBPACK_MODULE] (medium) [https://target.com/app.js] [./internal/module]

[SCOPED_PACKAGE] (low) [https://target.com/app.js] [@company/internal-api]

[JAVASCRIPT_PACKAGE] (low) [https://target.com/app.js] [lodash]

[OPEN_AI_USER_API_KEY] (medium) [https://api.target.com/script.js] [sk-4Fj28LmN0...]
```

---

## ⚠️ Disclaimer

This tool is for **educational purposes and authorized security testing only**.

Do not use against targets without permission.

---

## 👨‍💻 Author

**HunterDep**  
https://github.com/yHunterDep
