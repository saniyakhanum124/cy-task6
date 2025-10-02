# cy-task6
# Task 6 — Create a Strong Password and Evaluate Its Strength

**Objective:** Understand what makes a password strong and evaluate sample passwords using an online checker and a breach-check service.

## Tools used
- PasswordMeter (https://www.passwordmeter.com/) — online strength checker
- Have I Been Pwned (https://haveibeenpwned.com/Passwords) — breach lookup (k-anonymity)
- Screenshots of the results from the above sites

## Files included
- `screenshots(1).png` — PasswordMeter result for `pass123` (35%)
- `screenshots(2).png` — PasswordMeter result for `PassKlmpq123` (80%)
- `screenshots(3).png` — PasswordMeter result for `Password_check?123` (100%)
- `screenshots(4).png` — HaveIBeenPwned result for `Password_check?123` (Not found)
- `screenshots(5).png` — HaveIBeenPwned result for `pass123` (Pwned)

## Steps performed (exact)
1. Selected three test passwords (these are sample/test-only passwords and not used for any real accounts):
   - `pass123` (weak)
   - `PassKlmpq123` (moderate)
   - `Password_check?123` (strong)
2. Opened **PasswordMeter** and entered each password one-by-one, noted the percentage score and any suggestions shown on the page. Saved screenshots for each result.
3. Opened **Have I Been Pwned (Passwords)** and checked the first and third passwords to see whether they appear in public breach datasets. Saved screenshots of the results.

> **Safety note:** I only used sample passwords for testing. I did not use any real account passwords. Never paste a real account password into public sites or public repositories.

## Results summary 
| Test ID | Password (sample) | PasswordMeter score | HIBP breach check | Interpretation |
|---:|---|---:|---|---|
| 1 | pass123 | 35% | Pwned | Very weak: common and already in breaches. Must not use. |
| 2 | PassKlmpq123 | 80% | Not checked | Stronger: mixed case, length, numbers. Good but can be improved. |
| 3 | Password_check?123 | 100% | Not pwned | Very strong: length, symbols, mixed-case, numbers. Recommended (but avoid predictable words). |

## Short explanation of the findings
- **Why `pass123` is weak:** short, all-lowercase letters plus simple digits; commonly used and appears in breach lists — attackers can guess it quickly via dictionary attacks and brute force.
- **Why `PassKlmpq123` improved score:** added mixed case and more unique characters increases entropy; length helps.
- **Why `Password_check?123` got highest score:** includes upper/lowercase, digits, symbol, and is longer — increases entropy and estimated cracking time. However it contains the dictionary word "Password" which is predictable; better to use a non-dictionary passphrase or random words.

## Recommendations / Best practices
1. **Use length first:** prefer passwords of at least 12–16 characters for single-string passwords; passphrases (3–5 random words) are easier to remember and secure.  
2. **Avoid common words and predictable patterns:** using "password", keyboard patterns, or common substitutions (P@ssw0rd) are still guessable.  
3. **Use a combination:** mix upper/lowercase, numbers, and special characters when appropriate.  
4. **Prefer a password manager:** generate and store unique random passwords for each account (e.g., Bitwarden, KeePass).  
5. **Enable MFA (2FA):** adds a strong second layer of protection even if password is compromised.  
6. **Check breach exposure safely:** use HaveIBeenPwned's k-anonymity API or their web checker for sample passwords; do not paste real passwords into public tools.  
7. **Rotate or change passwords** if they appear in breach lists or after suspected compromise.

## How to reproduce (commands / steps)
- Visit https://www.passwordmeter.com/ → paste a sample password → read the percentage and notes → take screenshot.  
- Visit https://haveibeenpwned.com/Passwords → paste only test password → view results → screenshot.  
