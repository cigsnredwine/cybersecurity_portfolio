# Password Cracking with John the Ripper

## Overview

In this academic lab, I used John the Ripper on macOS to recover multiple passwords from instructor-provided DES and MD5 hash files. I practiced dictionary, rule-based, and incremental attacks and captured the results in screenshots, demonstrating the exposure created by weak and predictable passwords.

## Tools and Topics

- **John the Ripper:** Loading password hashes and reviewing recovered passwords.
- **Cracking techniques:** Dictionary attacks, wordlist rules, and incremental cracking.
- **Password security:** DES and MD5 password hashes, predictable passwords, and the limits of weak password choices.

## Workflow

1. **Set up the lab on macOS.** Installed and configured John the Ripper and used the instructor-provided `passwd.des` and `passwd.md5` files as inputs.
2. **Started with DES hashes.** Ran `john passwd.des` and monitored the terminal output as John recovered passwords and displayed their associated usernames.
3. **Observed the wordlist phase.** John used its bundled `password.lst` file with `Wordlist` rules to test candidate passwords and variations.
4. **Followed the incremental phase.** After the wordlist phase, John switched to `incremental:ASCII`. The DES run reported that its maximum candidate length was reduced to eight characters for that hash type.
5. **Repeated the process with MD5 hashes.** Ran `john passwd.md5` and observed the same progression through wordlist rules and incremental mode.
6. **Captured the results.** Saved screenshots of both runs showing recovered passwords and the transition between cracking modes.

## Results

The screenshots show **five recovered passwords in the DES run and four in the MD5 run**. Both runs recovered simple choices such as `123456`, `abc123`, and `qazwsx`; the DES screenshot also shows another password recovered after incremental mode began. These are the results visible at capture time, rather than final totals for completed runs.

## Materials

- [DES cracking screenshot](./screenshots/john-des-password-cracking.png)
- [MD5 cracking screenshot](./screenshots/john-md5-password-cracking.png)
- [Lab instructions](./Lab%20-%20Crack%20Encrypted%20Files%20%28%29.pdf)
- [Provided password hash files](./provided%20password%20files/)
