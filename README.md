# File-Handling--Made-Easy
Cartoonic depiction of File Handling codes &amp; modes.
# 🐍 Python File Handling - Visualization
By Irine Jeba | Tech Panda Academy, Chennai

> Two powerful visuals that made File Handling easy to remember forever!

## 📸 Image 1: The File Life Cycle - OPEN, WRITE, CLOSE
### 1. OPEN (The Start)
```python
my_file = open("secret_agent_notes.txt", "w")

### 2. WRITE (The Action)
```python
my_file.write("The secret password is: Bananas123")

### 3. CLOSE (The Finish)
```python
my_file.close()

**Smart Way (Auto-Close):**
```python
with open("secret_agent_notes.txt", "w") as my_file:
    my_file.write("The secret password is: Bananas123")
# No need to close - auto locked!

## 📸 Image 2: The 4 File Modes -r, w, a, x 
# r - Read
with open("notes.txt", "r") as f:
    print(f.read())

# w - Overwrite
with open("notes.txt", "w") as f:
    f.write("New content - old deleted!")

# a - Append
with open("notes.txt", "a") as f:
    f.write("\nThis line glued at end")

# x - Exclusive Create
with open("new_secret.txt", "x") as f:
    f.write("Created only once!")
with open("new_secret.txt", "x") as f:

