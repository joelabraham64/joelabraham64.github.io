---
layout: page
title: Spell Checker
description: Dictionary-based spell checker implemented in C using hash tables
img: assets/img/spellcheck.png
importance: 4
category: Software
---
**Source Code:**  
[View the project on GitHub](https://github.com/joelabraham/spellchecker)

## Overview

This project implements a **dictionary-based spell checker** in C using an **open-hashing (chaining) hash table** for efficient word lookup. The program reads a large dictionary file into memory and scans an input text file word by word, identifying misspelled words and generating correction suggestions.

The project emphasizes core systems programming concepts, including hashing, dynamic memory management, string processing, and efficient file I/O.

---

## How It Works

1. A dictionary file is read and stored in a hash table, where each bucket contains a linked list to handle collisions.
2. An input text file is read line by line and tokenized using common punctuation and whitespace delimiters.
3. Each word is checked against the dictionary:
   - If the word exists, it is considered valid.
   - If the word does not exist, it is reported as misspelled.
4. For each misspelled word, the program generates **suggestions** using simple edit operations such as:
   - Swapping adjacent characters
   - Removing the first or last character
   - Adding a single character (`a–z`) at the beginning or end
5. An optional command-line flag allows misspelled words to be **added to the dictionary at runtime**.

---

## Software Design

- **Hash table with chaining** is used for fast dictionary lookup
- **Linked lists** handle collisions within each hash bucket
- **String tokenization** is used to process input text accurately
- **Dynamic memory allocation** is carefully managed and freed at program termination

This design enables efficient processing of large text files while maintaining clear separation of responsibilities.

---

## Files

- `main.c` — Program control flow, file parsing, and spell-check logic  

---
