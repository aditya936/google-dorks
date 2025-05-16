# 🧠 Bug Bounty Google Dorks Collection

A curated list of Google dorks useful for finding responsible disclosure and bug bounty program pages.

---

## ✅ General Dorks

1. `"Last Updated: April"`  &nbsp;_// Specific month_

2. `site:*/*/responsible-disclosure | site:*/*/*/responsible-disclosure | site:*/*/*/*/responsible-disclosure | site:*/*/*/*/*/responsible-disclosure | site:*/responsible-disclosure-form | site:*/responsible-disclosure-form-*`

3. `site:*/responsible-disclosure-form | site:*/responsible-disclosure-form-*`

4. `"a token of our appreciation for helping"`

5. `site:*/*/vulnerability-disclosure | site:*/*/*/vulnerability-disclosure | site:*/*/*/*/vulnerability-disclosure | site:*/*/*/*/*/vulnerability-disclosure | site:*/vulnerability-disclosure-* | site:*/vulnerability-disclosure-form-*`

6. _Use different region domains (e.g. `.nl`, `.de`, `.jp`)_

7. `site:*/security.txt "bounty"`

8. `inurl:bounty "reward" "scope" "report" -yeswehack -hackerone -bugcrowd -synack -openbugbounty`

9. `"reward" "submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"`

10. `"submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone" -inurl:news -site:*.de`

---

## ✅ Dorks by AbhirupKonwar

11. `"The amount of the reward will be determined" "responsibledisclosure.nl" -site:responsibledisclosure.nl`

    `"we offer a reward for every report of a security"`

    `"following domains" "reward" "vulnerability" "policy"`

12. `"responsibledisclosure.nl" -site:responsibledisclosure.nl`

13. `"As a thank you for your help, we offer a reward"`

14. `"Floor Terra" "security" "vulnerability" "reward"`

    `"Floor Terra" "NCSC"`

    `"written by Floor Terra" -site:responsibledisclosure.nl -site:hackerone.com -site:github.com`

15. `"Whether we offer a reward" "vulnerability"`

16. `"reward" "We will respond to your report within"`

    `"reward" "We will respond to your report within" "we consider the security of our systems"`

17. `"If you are a security researcher" "reward"`  
    _Exclude platforms:_ `-site:hackerone.com -site:bugcrowd.com -site:yeswehack.com -site:intigriti.com`

    `"If you believe that you have found a security vulnerability on"`

18. `"The minimum reward will be" "Do not take advantage of the vulnerability"`

19. `"As a token of our gratitude for your assistance" "vulnerability"`

20. `"But no matter how much effort we put into system security"`

    `"If you find a vulnerability in our systems"`

    `"If you have found a weak spot in one of our systems"`

    `"we consider the security of our systems" "email your findings"`

21. `"Policy applies to all" "vulnerability"`

    `"Despite our efforts" "vulnerability" "security" "Email"`

    `"If you think you have identified a security vulnerability"`

    `"it is possible that a vulnerability" site:nl`

    `"This policy is intended to give security researchers"`

    `"The size of the reward" "vulnerability"`

    `"If you wish, we will mention your name" "vulnerability"`

    `"happy to issue a certificate" "vulnerability" "security"`

    `"We value the input of security researchers"`

    🔸 Creative Commons combinations:
    - `"Creative Commons Attribution" "vulnerability"`
    - `"Creative Commons Attribution" "security"`
    - `"Creative Commons Attribution" "offer"`
    - `"Creative Commons Attribution" "reward"`
    - `"Creative Commons Attribution" "token"`
    - `"Creative Commons Attribution" "bounty"`
    - `"Creative Commons Attribution" "certificate"`
    - `"Creative Commons Attribution" "hall of fame"`
    - `"Creative Commons Attribution" "wall of fame"`
    - `"Creative Commons Attribution" "gift"`
    - `"Creative Commons Attribution" "Email your findings"`

🧠 More dorks Written by [Abhirup Konwar](https://cybersecuritywriteups.com/non-english-dorks-to-find-bug-bounty-vdp-programs-d799f0a5161c)

---

## ✅ Additional Dorks

22. `"white hat program"`

23. `buy bitcoins "bug bounty"`

24. `inurl:bug bounty intext:"rupees" | inurl:responsible disclosure intext:"INR" | inurl:bug bounty intext:"₹"`

25. `"responsible disclosure" intext:"you may be eligible for monetary compensation"`

26. `title:"security" AND "Out of scope"`

27. `intext:security intext:"Wall of Fame:" AND "Out of scope"`

---

## 🔧 Top Sites security.txt Recon (To Be Automated Soon)

> I plan to create a bash script to automate this process soon.

Steps:

1. Download top 1,000,000 domains from [Cloudflare Radar](https://radar.cloudflare.com/domains)
2. Check both `/security.txt` and `/.well-known/security.txt` for each domain
3. Store the paths in a file (e.g., `paths.txt`)
4. Run the following commands:

```bash
cat domains.txt | httpx -path paths.txt -mc 200 -cl -ct -o result1.txt
cat domains.txt | while read d; do echo "www.$d"; done | httpx -path paths.txt -mc 200 -cl -ct -o result2.txt
