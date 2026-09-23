# File-Handling--Made-Easy
Cartoonic depiction of File Handling codes &amp; modes.
# 🐍 Python File Handling - Visual Cookie Book
By Irine Jeba | Tech Panda Academy, Chennai

> Two powerful visuals that made File Handling easy to remember forever!

## 📸 Image 1: The File Life Cycle - OPEN, WRITE, CLOSE

![Python File Office - Open Write Close](images/python-file-office.png)

**What this image shows:**

Imagine Python file handling is a government office with 3 staff members managing a Hard Drive cabinet.

### 1. OPEN (The Start)
```python
my_file = open("secret_agent_notes.txt", "w")

### 2. WRITE (The Action)
```python
my_file.write("The secret password is: Bananas123")

### 3. CLOSE (The Finish)
```python
my_file.close()
# Smart way - Auto close, no need to remember
with open("secret_agent_notes.txt", "w") as my_file:
    my_file.write("The secret password is: Bananas123")

## 📸 Image 2: The File Modes
# r - Read
with open("notes.txt", "r") as f:
    print(f.read())

# w - Write (Overwrite)
with open("notes.txt", "w") as f:
    f.write("New content - old deleted!")

# a - Append (Add at end)
with open("notes.txt", "a") as f:
    f.write("\nThis line is glued at end")

# x - Exclusive Create (Safe create)
with open("new_secret.txt", "x") as f:
    f.write("Created only once!")
