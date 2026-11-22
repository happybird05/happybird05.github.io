---
title: "Writeup Template"
date: 2026-11-22 00:00:00 +0900
categories: [writeup]
tags: [ctf, pwn]
ctf: "CTF Name 2026"
challenge_category: "pwn"
summary: "A template for CTF challenge writeups."
---

## Challenge Info

- **CTF:** CTF Name 2026
- **Challenge:** challenge-name
- **Category:** pwn / rev / web / crypto
- **Points / Solves:** 000 pts / 00 solves
- **Files:** `chall`, `libc.so.6`

## TL;DR

One or two sentences on the bug and how it was exploited.

## Analysis

- Binary protections (`checksec`)
- Program flow
- Vulnerable code

```c
// vulnerable function
```

## Exploitation

1. Leak
2. Primitive
3. Control flow hijack

```python
from pwn import *

p = process("./chall")
# exploit
p.interactive()
```

## Flag

```text
FLAG{...}
```

## Takeaways

What I learned and what to try next time.
