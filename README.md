<mark>Made with ChatGPT-5. For fun and testing purposes only.</mark>

# Command Line — Kali-style Terminal (Browser Sandbox)

Single-file terminal that runs **entirely in your browser**. Safe sandbox: **no commands run on your PC**; files persist in your browser (`localStorage`).

> Browser sandbox — does not run on your PC. Data stays in your browser. Type 'help' to list commands.

## Quick start
1. Open `command-line.html` in a modern browser.  
2. Type `help` to see commands.  
*(Optional)* Set prompt: `command-line.html?user=alice&host=kali`

## Features
- Kali-like UI & prompt (`user@host:[cwd]`)
- Virtual filesystem with persistence
- Tab autocomplete; Shift↑/Shift↓ history; Ctrl+L clear
- Works offline; no backend

## Built-in commands (high-level)
- **Files:** `ls [-la]`, `cd`, `pwd`, `touch`, `mkdir [-p]`, `rm [-r]`, `mv`, `cp [-r]`, `cat`, `head -n`, `tail -n`, `wc`, redirection `>` `>>`
- **Search:** `grep [-rni]`, `find <path> -name <pattern>`, `tree`
- **System:** `whoami`, `hostname`, `uname [-a]`, `date`, `cal`, `id`, `groups`, `uptime`, `basename`, `dirname`
- **Env:** `env`, `printenv [VAR]`, `export KEY=VALUE`, `which <cmd>`
- **Simulated:** `ps`, `top`, `ifconfig`, `ip a`, `ping [-c N] <host>`, `nmap <host>`, `apt update|install <pkg>`
- **Shell:** `history`, `clear`, `man <cmd>`, `help`

## Examples
~~~bash
whoami
ls -l /etc
grep -ni simulated /home/kali/README.txt
echo "hello" > /tmp/hello.txt && cat /tmp/hello.txt
~~~

**Note:** Networking/process/package commands are simulated for learning; nothing touches your real system.
