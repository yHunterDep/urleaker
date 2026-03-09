# What's URLeaker?
URLeaker is a tool that searches for sensitive information in HTML pages using regular expressions (regex).
Enjoy ;)

# Instalation
```sh
git clone https://github.com/yHunterDep/urleaker/
cd urleaker/
chmod +x urleaker
./urleaker -h
```

# How to use?
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
