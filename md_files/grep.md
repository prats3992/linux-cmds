# grep
### `grep` stands for global search for regular expression and printout.
### It searches a file for a particular pattern(RegEx) of characters and displays all lines that contain that pattern.

## Syntax
```bash
grep [OPTIONS] pattern file(s)
```
> ### [!NOTE]
> ### Run these commands on your local to see the color difference to understand the outputs.

| Regex Expression | Description                 | Example                |
|------------------|-----------------------------|------------------------|
| `^abc`           | Matches lines starting with "abc"   | `^abc123`              |
| `xyz$`           | Matches lines ending with "xyz"     | `123xyz`               |
| `a.b`            | Matches any character between "a" and "b"   | `a1b`, `a#b`          |
| `[0-9]`          | Matches any single digit     | `5`, `9`               |
| `[^aeiou]`       | Matches any character except vowels | `b`, `1`              |
| `ab*`            | Matches "a" followed by zero or more "b" | `a`, `ab`, `abb`      |
| `(abc\|def)`      | Matches either "abc" or "def" | `abc`, `def`           |
| `\d`             | Matches any digit            | `1`, `9`               |
| `\w`             | Matches any word character    | `a`, `3`, `_`          |
| `.*`             | Matches any sequence of characters | `abc123`, `xyz`      |
| `a+`             | Matches one or more occurrences of "a" | `a`, `aa`, `aaa`       |
| `\bword\b`       | Matches the whole word "word"      | `word`, `words`          |

### Example Usage
## Usage
```bash
cat lines.txt
1. The quick brown fox jumped over the lazy dog.
2. 3.14159265358979323846264338327950288419716939937510
3. Elephants are the largest land animals, with a gestation period of about 22 months.
4. In 2020, the global population was approximately 7.8 billion people.
5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
6. Bananas are berries, while strawberries are not, according to botanical classification.
7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
8. The mitochondria are often referred to as the powerhouse of the cell.
9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
11. The Eiffel Tower was completed in 1889 and stands at a height of 324 meters.
12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13. The Pacific Ocean is the largest and deepest ocean on Earth.
14. The human body has about 206 bones and 600 muscles.
15. The first computer programmer was Ada Lovelace, who worked on Charles Babbage's Analytical Engine.
```

### 1. Basic Usage
```bash
grep "is" lines.txt

5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13. The Pacific Ocean is the largest and deepest ocean on Earth.
```

### 2. Search for the pattern irrespective of the case
```bash
grep "IS" lines.txt -i

5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13. The Pacific Ocean is the largest and deepest ocean on Earth.
```

### 3. Count of number of matches
```bash
grep "is" lines.txt -c
6
```

### 4. Check for the whole word
See the output for `1` you will find that it even matched `is` when it was a part of `Lisa` so that is so counted but if you want to just check for the word `is` not parts of the words to get the pattern then,

```bash
grep "is" lines.txt -w

5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13. The Pacific Ocean is the largest and deepest ocean on Earth.
```

### 5. Get line number while displaying the output match
```bash
grep "is" lines.txt -n

5:5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
7:7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
9:9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10:10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
12:12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13:13. The Pacific Ocean is the largest and deepest ocean on Earth.
```

### 6. Search for multiple patterns at once
```bash
grep -e "is" -e "in" -e "by" lines.txt

5. The Mona Lisa, painted by Leonardo da Vinci, is housed in the Louvre Museum in Paris.
6. Bananas are berries, while strawberries are not, according to botanical classification.
7. The Great Wall of China is the longest wall in the world, stretching over 13,000 miles.
9. "To be or not to be, that is the question" is a famous soliloquy from Shakespeare's Hamlet.
10. Jupiter is the largest planet in our solar system and has a strong magnetic field.
11. The Eiffel Tower was completed in 1889 and stands at a height of 324 meters.
12. The platypus is a monotreme, a unique mammal that lays eggs instead of giving birth.
13. The Pacific Ocean is the largest and deepest ocean on Earth.
15. The first computer programmer was Ada Lovelace, who worked on Charles Babbage's Analytical Engine.
```

### 7. Search for a pattern in all the files recursively in a directory

```bash
grep -R "Elephant" .
./head.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./head.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./head.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./head.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./tail.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./grep.md:3. Elephants are the largest land animals, with a gestation period of about 22 months.
./lines.txt:3. Elephants are the largest land animals, with a gestation period of about 22 months.
```