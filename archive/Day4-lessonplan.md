# Cyber Squad - Day 4: Web Application Security (Hands-On and Legal)

**Platform:** U.S. Cyber Range Exercise Area, using an intentionally vulnerable practice web app hosted inside the isolated range.
**Duration:** about 4 hours.

---

## Learning objectives
- Explain how web requests work and where they break.
- Safely and legally practice finding common web flaws inside the range.
- Describe the defenses that stop these flaws.

## Vocabulary (acronyms expanded and defined)
- **HTTP / HTTPS / URL / HTML**: see Day 3 and the glossary.
- **XSS = Cross-Site Scripting**: getting a site to run attacker code in a victim's browser.
- **SQL = Structured Query Language**; **SQLi = SQL Injection**: smuggling commands into a database query.
- **OWASP = Open Worldwide Application Security Project**: a nonprofit that publishes the Top 10 web risks.
- **CSRF = Cross-Site Request Forgery**: tricking a logged-in user into making an unwanted request.
- **WAF = Web Application Firewall**: a filter that blocks malicious web traffic.

## Why a cyber range matters here
Web-attack practice must never be done against real websites you do not own. The U.S. Cyber Range provides isolated, intentionally vulnerable practice targets so students can learn legally and safely. Nothing leaves the range.

## Instructor setup
1. Launch a U.S. Cyber Range environment containing a deliberately vulnerable training web application (an instructor-selected practice app from the courseware or exercise catalog).
2. Confirm the app is reachable only inside the isolated lab network.
3. Restate the rules: these techniques are practiced only inside this range, only on these training targets.

## Student lab
1. Inspect requests: open the browser developer tools, view the page source, and examine a URL's query parameters.
2. Input handling: in the training app's search or login form, try a harmless test input and observe how the app responds. Discuss why trusting input is dangerous.
3. Map findings to the OWASP Top 10 and write, for each flaw you see, the matching defense (for example, parameterized queries for SQL injection, output encoding for XSS).

## Mini-lesson
```
  User input --> [ Web app ] --> [ Database ]
  If input is trusted as code, an attacker controls the query.
  Defense: treat input as DATA only (parameterized queries), validate, and encode output.
```

## In the news (real and verifiable)
Injection flaws such as SQL injection have appeared on the OWASP Top 10 list of critical web risks for many years, and OWASP now also publishes a Top 10 for Large Language Model applications. These lists are widely used by professional security teams, so the bugs students study here are the real ones companies defend against.

## Assessment
- MCQ: The best defense against SQL injection is a) longer passwords b) parameterized queries c) a faster server. (Answer: b.)
- Short answer: explain in one sentence why web-attack practice must stay inside a cyber range.
- Practical check: student lists three OWASP Top 10 items and a defense for each.

## Coding
Open **Day4.ipynb** for URL parsing, input-validation logic, and an AI prompt-injection mini-exercise.
