# head
#### The `head` command, as the name implies, prints the `top N` number of lines of the given input.
#### By default, it prints the `first 10 lines` of the specified files.
## Syntax
```bash
head [OPTION] filename(s)
```

## Example
#### We have the following file
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
### 1. Basic Default Usage
```bash
head lines.txt 
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
```

### 2. Specific number of lines using `-n number`
```bash
head lines.txt -n 4
1. The quick brown fox jumped over the lazy dog.
2. 3.14159265358979323846264338327950288419716939937510
3. Elephants are the largest land animals, with a gestation period of about 22 months.
4. In 2020, the global population was approximately 7.8 billion people.
```
### 3. Specific number of bytes using `-c num`
```bash
head lines.txt -c 200
1. The quick brown fox jumped over the lazy dog.
2. 3.14159265358979323846264338327950288419716939937510
3. Elephants are the largest land animals, with a gestation period of about 22 months.
4. In 20
```