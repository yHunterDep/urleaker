![urleaker](img.jpeg)

# What's URLeaker?
URLeaker is a tool that searches for sensitive information in HTML pages using regular expressions (regex).

# 💻 Instalation
```sh
git clone https://github.com/yHunterDep/urleaker/
cd urleaker/
pip install -r requirements.txt
chmod +x urleaker
./urleaker -h
```

# 🤔 How to use?
```sh
usage: urleaker [-h] -f FILE [-api] [-t] [-cr] [-k] [-g]
                [-html]

URLeaker - By HunterDep ^^

options:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  Put file to scan. Ex: -f urls-js.txt
  -api, --api           Find APIKeys (Google, AWS, Firebase,
                        etc)
  -t, --tokens          Find Tokens (Discord, Slack, Github,
                        etc)
  -cr, --credentials    Find Credentials (Email, passowrds,
                        etc)
  -k, --keys            Find private key
  -g, --generic         Find generic API Key
  -html, --html         Find intersting object html
```

# 📑 Scan All Urls
```sh
$ ./urleaker -f urls.txt
[PASSWORD] [https://site.com/js/storage/y.txt] [password=1234, password=admin123]
[EMAIL] [https://site.com/config.js] [admin@gmail.com, qwerty@gmail.com]
[GOOGLE_API_KEY] [https://site.com/api/v2/secret.js] [AIzaAab....]
```

# 🔐 Scan only ApiKeys
```sh
$ ./urleaker -f urls.txt -api
[GOOGLE_API_KEY] [https://site.com/api/v2/search] [AIzaPyb....]
[AWS_ACCESS_KEY] [https://site.com/old/users/config.json] [AKIA2CW....]
```

# 📑 Scan only Tokens
```sh
$ ./urleaker -f urls.txt -t
[DISCORD_TOKEN] [https://site.com/api/saas/config/my.js] [MNDOpdF...]
[JWT_TOKEN] [https://site.com/search] [eyJBrT...]
```

# 💻 Scan ApiKeys & Tokens
```sh
$ ./urleaker -f urls.txt -api -t
[GOOGLE_API_KEY] [https://site.com/api/v2/search] [AIzaPyb....]
[DISCORD_TOKEN] [https://site.com/api/saas/config/my.js] [MNDOpdF...]
```

Enjoy ;)
