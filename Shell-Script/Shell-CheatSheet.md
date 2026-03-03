# 🐚 Shell Scripting Cheat Sheet (DevOps Practical)

---

# 1️⃣ Script Basics

## Shebang
```bash
#!/bin/bash
```
**Description:** Defines interpreter.  
**Use:** Always first line in production scripts.

---

## Make Script Executable
```bash
chmod +x script.sh
```
**Description:** Adds execute permission.  
**Use:** Required before running with `./script.sh`.

---

## Run Script
```bash
./script.sh
bash script.sh
```
**Description:** Execute script.  
**Use:** `./` uses shebang, `bash` forces bash interpreter.

---

# 2️⃣ Variables & Arguments

## Declare Variable
```bash
NAME="Shashank"
```
**Description:** Stores value.  
**Use:** Store config, usernames, file paths.

---

## Access Variable
```bash
echo "$NAME"
echo "${NAME}"
```
**Description:** Prints variable value.  
**Use:** Always use quotes to prevent word splitting.

---

## Script Arguments
```bash
$0   # Script name
$1   # First argument
$#   # Number of arguments
$@   # All arguments
$?   # Last command exit status
```
**Use:** Input validation in automation scripts.

---

# 3️⃣ User Input

```bash
read NAME
read -p "Enter name: " NAME
read -sp "Enter password: " PASS
```
**Description:** Takes user input.  
**Use:** Interactive scripts (credentials, configs).

---

# 4️⃣ Conditionals

## If Statement
```bash
if [ condition ]; then
elif [ condition ]; then
else
fi
```
**Use:** Validation, checks before execution.

---

## String Comparison
```bash
[ "$a" = "$b" ]
[ -z "$a" ]
[ -n "$a" ]
```
**Use:** Input validation.

---

## Integer Comparison
```bash
[ $a -eq $b ]
[ $a -gt $b ]
[ $a -lt $b ]
```
**Use:** Monitoring thresholds (CPU, Disk).

---

## File Tests
```bash
[ -f file ]
[ -d dir ]
[ -e path ]
[ -s file ]
```
**Use:** Check file before backup/log parsing.

---

# 5️⃣ Loops

## For Loop
```bash
for i in 1 2 3; do
done
```
**Use:** Iterating servers, files, services.

---

## C Style Loop
```bash
for (( i=1; i<=5; i++ )); do
done
```
**Use:** Counter-based automation.

---

## While Loop
```bash
while [ condition ]; do
done
```
**Use:** Continuous monitoring.

---

# 6️⃣ Functions

```bash
my_function() {
}
```
**Description:** Reusable logic block.  
**Use:** Modular DevOps scripts.

---

## Return Code
```bash
return 0
```
**Use:** Success (0), Failure (!=0).

---

# 7️⃣ Arithmetic

```bash
result=$((5 + 3))
((counter++))
```
**Use:** Counters, calculations in monitoring.

---

# 8️⃣ Arrays

```bash
arr=("nginx" "docker")
echo "${arr[@]}"
echo "${#arr[@]}"
```
**Use:** Manage service lists or package installs.

---

# 9️⃣ Command Substitution

```bash
date=$(date)
host=$(hostname)
```
**Description:** Stores command output.  
**Use:** Logging with timestamps.

---

# 🔟 Redirection

```bash
command > file
command >> file
command 2> error.log
command &> all.log
```
**Use:** Logging automation output.

---

# 1️⃣1️⃣ grep (Search)

```bash
grep "error" file
grep -i "error" file
grep -r "text" dir
grep -n "text" file
grep -c "error" file
```
**Description:** Pattern search tool.  
**Use:** Log analysis, troubleshooting.

---

# 1️⃣2️⃣ awk (Column Processing)

```bash
awk '{print $1}' file
awk -F: '{print $1}' /etc/passwd
awk '$3 > 80 {print $1}' file
```
**Description:** Advanced text processing.  
**Use:** Extract CPU %, usernames, log fields.

---

# 1️⃣3️⃣ sed (Edit Stream)

```bash
sed 's/old/new/g' file
sed -i 's/old/new/g' file
sed '/pattern/d' file
```
**Description:** Modify text in stream/file.  
**Use:** Config updates in bulk.

---

# 1️⃣4️⃣ cut

```bash
cut -d: -f1 file
cut -c1-10 file
```
**Use:** Extract specific columns.

---

# 1️⃣5️⃣ sort & uniq

```bash
sort file
sort -n file
uniq -c file
```
**Use:** Log frequency analysis.

---

# 1️⃣6️⃣ tr

```bash
tr 'a-z' 'A-Z'
tr -d '0-9'
```
**Use:** Format/clean data.

---

# 1️⃣7️⃣ wc

```bash
wc -l file
wc -w file
```
**Use:** Count logs, lines, words.

---

# 1️⃣8️⃣ head / tail

```bash
head -n 5 file
tail -n 10 file
tail -f log.txt
```
**Use:** Monitor logs in real time.

---

# 1️⃣9️⃣ find

```bash
find /path -name "*.log"
find /path -mtime +7 -delete
```
**Use:** Delete old logs, search files.

---

# 2️⃣0️⃣ tar & gzip

```bash
tar -czf backup.tar.gz folder/
gzip file.log
```
**Use:** Backup automation.

---

# 2️⃣1️⃣ Strict Mode (Production Best Practice)

```bash
set -e
set -u
set -o pipefail
set -euo pipefail
```
**Use:** Prevent silent failures in production scripts.

---

# 2️⃣2️⃣ Debug Mode

```bash
set -x
```
**Use:** Troubleshooting script execution.

---

# 2️⃣3️⃣ trap (Cleanup)

```bash
trap cleanup EXIT
```
**Use:** Auto cleanup temp files.

---

# 2️⃣4️⃣ Cron Format

```
* * * * * command
│ │ │ │ │
│ │ │ │ └── Day of week
│ │ │ └──── Month
│ │ └────── Day
│ └──────── Hour
└────────── Minute
```

Example:
```bash
0 2 * * * /backup.sh
```
**Use:** Schedule automation jobs.

---

# 🚀 DevOps Best Practices

- Always use `set -euo pipefail`
- Always quote variables `"${VAR}"`
- Validate arguments before execution
- Log important actions
- Use functions for reusable code

---

# #90DaysOfDevOps
# Shell for DevOps Engineers