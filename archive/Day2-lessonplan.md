# Cyber Squad - Day 2: Accounts, Passwords, and Hashing

**Platform:** U.S. Cyber Range Exercise Area (Linux environment).
**Duration:** about 4 hours.

---

## Learning objectives
- Explain the CIA triad and authentication.
- Understand how passwords are stored as hashes, not plain text.
- Observe why weak passwords fall quickly, using safe in-range practice data only.

## Vocabulary (acronyms expanded and defined)
- **CIA triad = Confidentiality, Integrity, Availability**.
- **Authentication**: proving who you are.
- **MFA = Multi-Factor Authentication**: two or more proofs of identity.
- **Hash**: a one-way fingerprint of data.
- **Salt**: random data added before hashing so identical passwords get different hashes.
- **Brute force**: trying every possible password.

## Instructor setup
1. From the U.S. Cyber Range Exercise Area, launch a Linux environment that includes standard command-line tools.
2. Prepare a practice file of sample hashes that you generate yourself for class (never use real user data). Keep all activity inside the isolated range.
3. Reinforce the ethics rule: cracking is practiced only on data you created or were given permission to use.

## Student lab
1. See how Linux stores account information:
   - `cat /etc/passwd` lists accounts (no passwords here).
   - Password hashes live in `/etc/shadow`, readable only by the administrator. Discuss why.
2. Make and inspect a hash with Python (in the terminal or notebook):
   - `python3 -c "import hashlib;print(hashlib.sha256(b'sunshine').hexdigest())"`
   - Change one letter and watch the entire hash change.
3. Discuss salting: hash `password` twice with two different salts and compare the results.

## Mini-lesson: why length wins
```
  Possible passwords = N ** L   (N = character set size, L = length)
  Add length -> the number explodes far faster than adding symbols.
```

## In the news (real and verifiable)
Annual reports from password managers such as NordPass repeatedly find that simple passwords like 123456 remain among the most common in the world, and these are cracked almost instantly. Major past breaches led to the practice of storing salted hashes rather than plain passwords, and to the wide push for multi-factor authentication.

## Assessment
- Numerical: how many 6-digit PINs exist using digits 0 to 9? (Answer: 1,000,000.)
- MCQ: A salt is used to a) speed up logins b) make identical passwords hash differently c) encrypt files. (Answer: b.)
- Practical check: student shows two different hashes for the same word using two salts.

## Coding
Open **Day2.ipynb** for the hashing and password-entropy exercises.
