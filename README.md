<h1 align="center">🔍 URLeaker</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/yHunterDep/urleaker/main/urleaker.png" width="300"/>
</p>

<p align="center">
  <b>A powerful secret scanner for HTTP responses</b><br>
  API Keys • Tokens • Credentials • Misconfigurations
</p>

<p align="center">
  <a href="https://github.com/yHunterDep/urleaker">
    <img src="https://img.shields.io/badge/status-active-brightgreen?style=for-the-badge">
  </a>
  <a href="https://github.com/yHunterDep/urleaker">
    <img src="https://img.shields.io/badge/version-0.2.0-blue?style=for-the-badge">
  </a>
  <a href="https://www.python.org/">
    <img src="https://img.shields.io/badge/python-3.x-purple?style=for-the-badge">
  </a>
</p>

---

## 💻 Terminal Preview

<pre style="background-color:#000000;color:#ffffff;padding:16px;border-radius:8px;overflow-x:auto;">
$ ./urleaker -h
usage: urleaker [-h] -f FILE [-sv SEVERITIES] [-api] [-t] [-cr] [-k] [-g]
                [-html] [-c CONCURRENT] [-s] [-nc]

URLeaker - By HunterDep ^^

options:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  Put file to scan. Ex: -f urls-js.txt
  -sv SEVERITIES, --severities SEVERITIES
                        Choice severities to scan (-sv
                        unknown,low,medium,high,critical)
  -api, --api           Find APIKeys (Google, AWS, Firebase, etc)
  -t, --tokens          Find Tokens (Discord, Slack, Github, etc)
  -cr, --credentials    Find Credentials (Email, passowrds, etc)
  -k, --keys            Find private key
  -g, --generic         Find generic API Key
  -html, --html         Find intersting object html
  -c CONCURRENT, --concurrent CONCURRENT
                        Number of concurrent threads (default: 20)
  -s, --silent          Skip banner mode                                           -nc, --no_color       Remove colors from output
  
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
./urleaker -f urls.txt -api
```

```bash
./urleaker -f urls.txt -t
```

```bash
./urleaker -f urls.txt -cr
```

```bash
./urleaker -f urls.txt -sv high,critical
```

```bash
./urleaker -f urls.txt -t -api
```

```bash
./urleaker -f urls.txt -c 50
```

```bash
./urleaker -f urls.txt -s
```

```bash
./urleaker -f urls.txt -nc
```

---

## 🧠 Features

- 🌐 Scans **any HTTP response body** (not limited to JS)
- 🔑 API Key detection (AWS, Google, Stripe, etc)
- 🔐 Token leaks (Discord, GitHub, Slack, JWT)
- 📧 Credentials (emails, passwords, FTP)
- 🔒 Private keys detection
- 🧩 Generic secrets & misconfig patterns
- ⚡ Multithreaded scanning
- 🎯 Severity filtering (low → critical)

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
[AWS_SECRET_KEY] (high) [https://target.com/api] [ABCD1234...]

[DISCORD_TOKEN] (critical) [https://target.com/script.js] [MTIzNDU2...]

[EMAIL] (info) [https://target.com/page] [admin@example.com]
```

---

## ⚠️ Disclaimer

This tool is for **educational purposes and authorized security testing only**.

Do not use against targets without permission.

---

## 👨‍💻 Author

**HunterDep**  
https://github.com/yHunterDep
