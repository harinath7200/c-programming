# Python Tutorial Exercises

This beginner-friendly tutorial uses a repeatable exercise pattern:

1. **Learn** a small idea.
2. **Try** the exercise without looking at the answer.
3. **Check** your result against the expected output.
4. **Review** the sample solution and improve your own version.

## Getting started

Install Python 3, then create a folder for your work and run each exercise with:

```bash
python3 exercise_01.py
```

Use a separate file for every exercise. Type the programs yourself rather than
copying the solutions; debugging small mistakes is part of the learning process.

## Progress tracker

| Exercise | Topic | Done |
| --- | --- | --- |
| 1 | Output and variables | ⬜ |
| 2 | Input and numbers | ⬜ |
| 3 | Decisions | ⬜ |
| 4 | Loops | ⬜ |
| 5 | Lists | ⬜ |
| 6 | Functions | ⬜ |
| 7 | Dictionaries | ⬜ |
| 8 | Files | ⬜ |

---

## Exercise 1 — Introduce yourself

**Learn:** `print()` displays text, and variables store values.

**Try:** Create `exercise_01.py`. Store your name and favourite hobby in
variables. Print a two-line introduction using those variables.

**Example output:**

```text
Hello, I am Ada.
I enjoy solving puzzles.
```

**Challenge:** Change the program so it prints the name in uppercase.

<details>
<summary>Sample solution</summary>

```python
name = "Ada"
hobby = "solving puzzles"

print(f"Hello, I am {name}.")
print(f"I enjoy {hobby}.")
```
</details>

---

## Exercise 2 — Add two numbers

**Learn:** `input()` returns text. Convert numeric input with `int()` before
performing arithmetic.

**Try:** Ask the user for two whole numbers and print their sum.

**Example run:**

```text
First number: 7
Second number: 5
Total: 12
```

**Challenge:** Also print the product of the two numbers.

<details>
<summary>Sample solution</summary>

```python
first = int(input("First number: "))
second = int(input("Second number: "))

print(f"Total: {first + second}")
```
</details>

---

## Exercise 3 — Even or odd?

**Learn:** An `if` statement runs code only when its condition is true. The
remainder operator (`%`) helps identify even numbers.

**Try:** Ask for a whole number. Print `even` when it is divisible by 2;
otherwise print `odd`.

**Example run:**

```text
Number: 19
19 is odd.
```

**Challenge:** Print a special message when the number is zero.

<details>
<summary>Sample solution</summary>

```python
number = int(input("Number: "))

if number % 2 == 0:
    print(f"{number} is even.")
else:
    print(f"{number} is odd.")
```
</details>

---

## Exercise 4 — Countdown

**Learn:** A `for` loop repeats code for every value from `range()`.

**Try:** Print a countdown from 5 to 1, then print `Lift off!`.

**Expected output:**

```text
5
4
3
2
1
Lift off!
```

**Challenge:** Ask the user which number the countdown should begin with.

<details>
<summary>Sample solution</summary>

```python
for number in range(5, 0, -1):
    print(number)

print("Lift off!")
```
</details>

---

## Exercise 5 — Find the largest score

**Learn:** Lists hold multiple values. `max()` returns the largest item in a
list.

**Try:** Given the list below, print the highest score and the average score.

```python
scores = [78, 91, 85, 88, 95]
```

**Expected output:**

```text
Highest score: 95
Average score: 87.4
```

**Challenge:** Let the user add one more score before calculating the results.

<details>
<summary>Sample solution</summary>

```python
scores = [78, 91, 85, 88, 95]

highest = max(scores)
average = sum(scores) / len(scores)

print(f"Highest score: {highest}")
print(f"Average score: {average}")
```
</details>

---

## Exercise 6 — Write a reusable greeting

**Learn:** Functions group reusable behaviour. Parameters allow a function to
receive values.

**Try:** Write a function named `greet` that accepts a name and prints a
friendly greeting. Call it for three different names.

**Example output:**

```text
Welcome, Ada!
Welcome, Lin!
Welcome, Sam!
```

**Challenge:** Add a second parameter for the time of day.

<details>
<summary>Sample solution</summary>

```python
def greet(name):
    print(f"Welcome, {name}!")


greet("Ada")
greet("Lin")
greet("Sam")
```
</details>

---

## Exercise 7 — Contact lookup

**Learn:** Dictionaries connect a key to a value. Use square brackets to look
up a known key and `.get()` when the key might be missing.

**Try:** Create a dictionary that maps three names to phone numbers. Ask the
user for a name and print that person's number, or `Contact not found.` when
the name is absent.

**Example run:**

```text
Name: Ada
555-0101
```

**Challenge:** Store both a phone number and an email address for each contact.

<details>
<summary>Sample solution</summary>

```python
contacts = {
    "Ada": "555-0101",
    "Lin": "555-0102",
    "Sam": "555-0103",
}

name = input("Name: ")
number = contacts.get(name)

if number is None:
    print("Contact not found.")
else:
    print(number)
```
</details>

---

## Exercise 8 — Save a note

**Learn:** A `with` block closes a file automatically. Opening a file with
`"w"` writes new content.

**Try:** Ask the user for a short note. Save it to `note.txt`, then read the
file and print its contents.

**Example run:**

```text
Write a note: Practice Python every day.
Saved note: Practice Python every day.
```

**Challenge:** Use append mode (`"a"`) to keep previous notes instead of
replacing them.

<details>
<summary>Sample solution</summary>

```python
note = input("Write a note: ")

with open("note.txt", "w", encoding="utf-8") as file:
    file.write(note)

with open("note.txt", encoding="utf-8") as file:
    saved_note = file.read()

print(f"Saved note: {saved_note}")
```
</details>

## Next steps

Repeat the same pattern for each new topic: state the goal, try a small program,
check the result, and add one challenge. Good follow-up topics are error
handling, modules, classes, and automated tests.
