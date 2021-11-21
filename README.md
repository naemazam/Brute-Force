<p align="center">
  <h1 align="center">Brute Force
</h1>
  <p align="center"> Understand Brute Force Password attack  </p>
</p> 

## Simple Knowledge

## What is that?
A brute force attack is a hacking method that uses trial
 and error to crack passwords, login credentials, and encryption keys.
 The hacker tries multiple usernames and passwords, often using a computer to test a wide range of combinations, until they find the correct login information.

## What do hackers gain from Brute Force Attacks?
Brute force attackers have to put in a bit of effort to make these schemes pay off. While technology does make it easier, you might still question: why would someone do this?

Here’s how hackers benefit from brute force attacks:

- Profiting from ads or collecting activity data
- Stealing personal data and valuables
- Spreading malware to cause disruptions
- Hijacking your system for malicious activity
- Ruining a website’s reputation

## Types of Brute Force Attacks
Each brute force attack can use different methods to uncover your sensitive data. You might be exposed to any of the following popular brute force methods:

- Simple Brute Force Attacks
- Dictionary Attacks
- Hybrid Brute Force Attacks
- Reverse Brute Force Attacks
- Credential Stuffing

## Steps to Protect Passwords for Professionals
To keep yourself and your network safe, you'll want to take your precautions and help others do so as well. User behavior and network security systems will both need reinforcement.

For IT specialists and users alike, you’ll want to take a few general pieces of advice to heart:

- Use an advanced username and password. Protect yourself with credentials that are stronger than admin and password1234 to keep out these attackers. The stronger this combination is, the harder it will be for anyone to penetrate it.
- Remove any unused accounts with high-level permissions. These are the cyber equivalent of doors with weak locks that make breaking in easy. Unmaintained accounts are a vulnerability you can’t risk. Throw them away as soon as possible.
- Once you’ve got the basics down, you’ll want to bolster your security and get users on board.

- We’ll begin with what you can do on the backend, then give tips to support safe habits.

- Passive Backend Protections for Passwords
- High encryption rates: to make it harder for brute force attacks to succeed, system administrators should ensure that passwords for their systems are encrypted with the highest encryption rates possible, such as 256-bit encryption. The more bits in the encryption scheme, the harder the password is to crack.

- Salt the hash: administrators should also randomize password hashes by adding a random string of letters and numbers (called salt) to the password itself. This string should be stored in a separate database and retrieved and added to the password before it's hashed. By salting the hash, users with the same password have different hashes.

- Two-factor authentication (2FA): additionally, administrators can require two-step authentication and install an intrusion detection system that detects brute force attacks. This requires users to follow-up a login attempt with a second factor, like a physical USB key or fingerprint biometrics scan.

- Limit number of login re-tries: limiting the number of attempts also reduces susceptibility to brute-force attacks. For example, allowing three attempts to enter the correct password before locking out the user for several minutes can cause significant delays and cause hackers to move on to easier targets.

- Account lockdown after excessive login attempts: if a hacker can endlessly keep retrying passwords even after a temporary lockout, they can return to try again. Locking the account and requiring the user to contact IT for an unlock will deter this activity. Short lockout timers are more convenient for users, but convenience can be a vulnerability. To balance this, you might consider using the long-term lockdown if there are excessive failed logins after the short one.

- Throttle rate of repeated logins: you can further slow an attacker’s efforts by creating space between each single login attempt. Once a login fails, a timer can deny login until a short amount of time has passed. This will leave lag-time for your real-time monitoring team to spot and work on stopping this threat. Some hackers might stop trying if the wait is not worth it.

- Required Captcha after repeated login attempts: manual verification does stop robots from brute-forcing their way into your data. Captcha comes in many types, including retyping the text in an image, checking a checkbox, or identifying objects in pictures. Regardless of what you use, you can use this before the first login and after each failed attempt to protect further.

- Use an IP denylist to block known attackers. Be sure that this list is constantly updated by those who manage it.

## Active IT Support Protections for Passwords
- Password education: user behavior is essential to password security. Educate users on safe practices and tools to help them keep track of their passwords. Services like Kaspersky Password Manager allow users to save their complex, hard-to-remember passwords in an encrypted “vault” instead of unsafely writing them down on sticky notes. Since users tend to compromise their safety for the sake of convenience, be sure to help them put convenient tools in their hands that will keep them safe.

- Watch accounts in real-time for strange activity: Odd login locations, excessive login attempts etc. Work to find trends in unusual activity and take measures to block any potential attackers in real-time. Look out for IP address blocks, account lockdown, and contact users to determine if account activity is legitimate (if it looks suspicious).

- How Users Can Strengthen Passwords Against Brute Force Attacks
- As a user, you can do a lot to support your protection in the digital world. The best defense against password attacks is ensuring that your passwords are as strong as they can be.

- Brute force attacks rely on time to crack your password. So, your goal is to make sure your password slows down these attacks as much as possible, because if it takes too long for the breach to be worthwhile… most hackers will give up and move on.

## Here are a few ways you can strength passwords against brute attacks:

- Longer passwords with varied character types. When possible, users should choose 10-character passwords that include symbols or numerals. Doing so creates 171.3 quintillion (1.71 x 1020) possibilities. Using a GPU processor that tries 10.3 billion hashes per second, cracking the password would take approximately 526 years. Although, a supercomputer could crack it within a few weeks. By this logic, including more characters makes your password even harder to solve.

- Elaborate passphrases. Not all sites accept such long passwords, which means you should choose complex passphrases rather than single words. Dictionary attacks are built specifically for single word phrases and make a breach nearly effortless. Passphrases — passwords composed of multiple words or segments — should be sprinkled with extra characters and special character types.

- Create rules for building your passwords. The best passwords are those you can remember but won’t make sense to anyone else reading them. When taking the passphrase route, consider using truncated words, like replacing “wood” with “wd” to create a string that makes sense only to you. Other examples might include dropping vowels or using only the first two letters of each word.

- Stay away from frequently used passwords. It's important to avoid the most common passwords and to change them frequently.

- Use unique passwords for every site you use. To avoid being a victim of credential stuffing, you should never reuse a password. If you want to take your security up a notch, use a different username for every site as well. You can keep other accounts from getting compromised if one of yours is breached.

- Use a password manager. Installing a password manager automates creating and keeping track of your online login info. These allow you to access all your accounts by first logging into the password manager. You can then create extremely long and complex passwords for all the sites you visit, store them safely, and you only have to remember the one primary password.



## Python Code 
In Here We Try to undestand How it Work With Python . Enter a password  And It will Show How it Crack Password.

Copy code and test on Any Editor



```Python
paswd = input("Insert Password: \n")
def Brute(paswd):
   print("[+][+] Starting Brute Force...")
   charset= list("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789")
   result=""
   x=0
   while x<=len(paswd)-1:
      for char in charset:
         pchar=paswd[x]
         if char==pchar:
           print("[+] Trying...", char)
           print("[+][+]Matched (",char, ")")
           result+=char
           x+=1
           break
         else:
           print("[+] Trying...",char)     
   print("[+][+] All Matched - Password Found:", result)
Brute(paswd) 

```


## Demo 
Input Password abc

output

```python
Insert Password: 
[+][+] Starting Brute Force...
[+] Trying... a
[+][+]Matched ( a )
[+] Trying... a
[+] Trying... b
[+][+]Matched ( b )
[+] Trying... a
[+] Trying... b
[+] Trying... c
[+][+]Matched ( c )
[+][+] All Matched - Password Found: abc
```
