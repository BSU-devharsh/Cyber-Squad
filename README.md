# Cyber Squad: A Five-Day Cybersecurity Camp on the U.S. Cyber Range

A hands-on, instructor-led cybersecurity summer camp for middle and high school students. It pairs the **U.S. Cyber Range** (operated by Virginia Tech) for safe, isolated, cloud-based labs with interactive slide decks, Python notebooks, and free security games.

Every day has three activities: **one Python exercise, one Cyber Range lab, and one interactive game.**

A free, browser-only edition that uses only public tools is provided separately in the `cyberquest-camp` folder.

## How it is organized
- `Interactive_Slides.html` is the **main course deck (150 slides)**: the full lecture with bonus content, figures, and exercises. It opens with how the camp works and, at marked points, sends you to that day's deck, notebook, and Cyber Range lab. A Day decks menu (top right) links to each day deck.
- Each `DayN/` folder holds exactly two files:
  - `DayN_slides.html` - a **50-slide day deck** (overview, lecture, Python exercise, Cyber Range lab, game, quiz, wrap up).
  - `DayN.ipynb` - the day's **Python exercise** notebook.

## Five-day plan

| Day | Focus | Cyber Range lab | Python exercise | Game |
|-----|-------|-----------------|-----------------|------|
| 1 | Linux and networking foundations | Launch a Linux VM, use the terminal | Variables, loops, subnet math | CodeCombat, OverTheWire Bandit |
| 2 | Accounts, passwords, hashing | Inspect /etc/passwd and hashing | Keyspace, crack time, salting | Google Interland |
| 3 | Cryptography and traffic analysis | Wireshark: HTTP vs HTTPS | Caesar, Base64, XOR, hashing | dcode.fr, CyberChef |
| 4 | Web application security | Isolated vulnerable web app | URL parsing, input validation, AI guard | CTFLearn, Lakera Gandalf |
| 5 | Capstone CTF and blue-team defense | Team CTF and log triage | Decode flags, log analysis | picoCTF |

## What you need
- An **educator account** on the U.S. Cyber Range. See https://www.uscyberrange.org/ for sign-up, the Courseware Repository, and **Course 6302: Cybersecurity Fundamentals**. Confirm current pricing and any K-12 or academic options on the official site before committing.
- A modern web browser. The slide decks are plain HTML (open `Interactive_Slides.html`). The notebooks run free in Google Colab (upload `DayN.ipynb`) or in Jupyter.

## Why a cyber range
A cyber range is an isolated, cloud-hosted practice lab. Students run real tools (the Linux terminal, Wireshark, vulnerable practice web apps, Capture The Flag environments) without touching the public internet or any real victim. It is the responsible way to teach offensive and defensive skills.

## Safety and ethics
- Only practice on the Cyber Range training targets your instructor provides, or on the listed learning sites.
- Never test attacks on systems you do not own or do not have permission to test. Doing so can violate the Computer Fraud and Abuse Act (CFAA).
- Never enter a real password into any tester. Use made-up examples.

## Repository structure
```
Cyber Squad/
  README.md  LICENSE  CITATION.cff
  Interactive_Slides.html        (main deck, 150 slides, + Day decks menu)
  Day1/  Day1_slides.html  Day1.ipynb
  Day2/  Day2_slides.html  Day2.ipynb
  Day3/  Day3_slides.html  Day3.ipynb
  Day4/  Day4_slides.html  Day4.ipynb
  Day5/  Day5_slides.html  Day5.ipynb
  instructor/   (setup guide, safety and ethics, rubric, glossary)
  resources/    (supplementary handouts)
  archive/      (earlier source materials, kept for reference)
```

## Citation
See `CITATION.cff`. Repository: https://github.com/BSU-devharsh/Cyber-Squad

## License
MIT (see `LICENSE`). External tools and the U.S. Cyber Range keep their own terms and licenses.
