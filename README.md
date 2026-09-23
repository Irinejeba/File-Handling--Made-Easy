### 🐍 File Handling Made Easy - Full Code by Irine Jeba

## Image 1: OPEN -> WRITE -> CLOSE

![Image 1 - Lifecycle](File%20Handling%20codes.jpg)

### 1. OPEN - Blue Staff takes file from OPEN basket
```python
my_file = open("secret_agent_notes.txt", "w")
print("1. File OPENED")
```

### 2. WRITE - Middle Staff writes secret
```python
my_file.write("The secret password is: Bananas123")
print("2. Data WRITTEN")
```

### 3. CLOSE - Third Staff locks and puts in OUT basket
```python
my_file.close()
print("3. File CLOSED")
```

### Pro Tip - Smart way (auto-close) - No need to close manually
```python
with open("secret_agent_notes.txt", "w") as my_file:
    my_file.write("The secret password is: Bananas123 - Smart way")
print("Smart way done - Auto closed!")
```

## Image 2: 4 Modes - r, w, a, x

![Image 2 - Modes](File%20Handling%20modes.jpg)

### r - Inspector - READ ONLY
```python
print("--- r - Inspector (read only) ---")
with open("secret_agent_notes.txt", "r") as f:
    content = f.read()
    print(f"f.read = {content}")
```

### w - Vaporizer - WRITE (deletes old)
```python
print("--- w - Vaporizer (deletes old, writes new) ---")
with open("notes.txt", "w") as f:
    f.write("New content - old deleted!")
print("Created notes.txt with w mode")
```

### a - Continuator - APPEND (keeps old)
```python
print("--- a - Continuator (keeps old, adds at end) ---")
with open("notes.txt", "a") as f:
    f.write("\nThis line is glued at end")
print("Appended to notes.txt with a mode")
```

### x - Perfectionist - EXCLUSIVE CREATE
```python
print("--- x - Perfectionist (new only) ---")
try:
    with open("new_secret.txt", "x") as f:
        f.write("Created only once!")
    print("Created new_secret.txt with x mode - First time success")
except FileExistsError:
    print("File already exists! x mode prevents overwrite - Safe!")
```

### Final check - read everything
```python
print("\n=== Final Check ===")
with open("notes.txt", "r") as f:
    print("notes.txt content:")
    print(f.read())
```
