# Attacks and Defenses - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Cryptography Concepts

## 🎯 Objective


## 🧠 Core Concepts Learned
## Cryptography Concepts

### Why Cryptography Matters
- Data doesn't travel directly from you to the recipient. It bounces through dozens of computers and routers along the way. Without protection, anyone with access to those systems could read, change, or block your data.
- Cryptography solves this by using mathematical rules and secret keys to scramble information into gibberish that only authorised people can unscramble.

### Understanding the Basics
- Before we jump into symmetric encryption, let's define the core terms we'll use throughout this room:

    Plaintext - A message you can read normally. Like HELLO or Patient name: Alice Smith.

    Ciphertext - A scrambled version that's not supposed to make sense. Like KHOOR or Sdwlhqw qdph: Dolfh Vplwk.

    Key - The secret ingredient that controls how scrambling and unscrambling work. Think of it as a password that the algorithm uses.

    Algorithm - The public recipe—the set of steps that explain how to use the key on the message. Everyone can know the algorithm. Security comes from keeping the key secret.

- Encryption process: plaintext + encryption algorithm + key  → ciphertext
- Decryption process: ciphertext + decryptiong algorithm + key   → plaintext

#### The lockbox Analogy
 Alice wants to send Bob a secret letter, but it must go through the public postal system, where anyone could open it and read it.
Here's what she does:

    She writes her message (the plaintext) on paper.
    She puts the letter in a sturdy lockbox.
    She locks it with a padlock using her key.
    She sends the locked box (the ciphertext) through the mail.

When Bob gets the box, he uses his copy of the same key to unlock it and read the message. Anyone who intercepts the box along the way sees a locked metal box. Without the key, it's useless. The message stays private.

### Plaintext versus Ciphertext

Now, how does this look when dealing with text or data? Say Alice wants to send:

HELLO

That's the plaintext—the readable message.

Alice uses an algorithm and a secret key to scramble it. After scrambling, it becomes:

KHOOR

That's the ciphertext. To anyone without the key, KHOOR is meaningless. The key point: ciphertext should look like random nonsense to anyone who doesn't have the key.

Bob receives KHOOR, uses the same key and algorithm, and unscrambles it back to HELLO.

#### The Caesar Cipher: Algorithm Plus Key
The Caesar cipher is named after Julius Caesar, who reportedly used this technique over 2000 years ago to send military messages. Even back then, people understood the value of keeping communications secret.

How It Works

The Caesar cipher shifts each letter in your message by a fixed number of positions in the alphabet. That fixed number is your key.
If Alice wants to encrypt HELLO with a key of 3:

    H → K
    E → H
    L → O
    L → O
    O → R

So HELLO becomes KHOOR.

To decrypt KHOOR, Bob shifts each letter backwards by 3:

    K → H
    H → E
    O → L
    O → L
    R → O

He gets HELLO again. Magic? Nope. Math.

With the Caesar cipher:

    The algorithm (shift each letter by some number) is completely public. Everyone can know how it works.
    The key (the number 3 in our example) is what's secret. Only Alice and Bob know this number.

Here's the thing: The Caesar cipher is not secure and is never used in real systems. It's way too easy to compromise and decrypt messages. We're using it here purely because it's simple to understand and shows you how keys and algorithms work together.

## Symmetric Encryption - Hiding Information
That's symmetric encryption in a nutshell: one key locks the box, the same key unlocks it.

The Caesar cipher is an example of symmetric encryption. This means that:

    The same key encrypts (locks) and decrypts (unlocks) the message.
    Both sender and receiver need a copy of that key.
    The key has to stay secret from everyone else.

Some of the benefits of using symmetric encryption are:

    It's fast. Symmetric algorithms can churn through huge amounts of data really quickly.
    It's efficient. Perfect for encrypting files, hard drives, and network traffic where speed matters.

However, there's a catch to this efficiency:

    How do Alice and Bob share that key safely in the first place?

If they send the key over the internet in plain view, an eavesdropper can grab it. Then that eavesdropper can decrypt every future message.

You might think, "Just encrypt the key!",  but then you'd need another key to encrypt that key, and then another key for that key, and you see the problem. Infinite regress.

This is called the key distribution problem, and it's the Achilles' heel of symmetric encryption when used alone.

We'll solve this in the next task with asymmetric encryption—a clever approach that uses two different keys instead of one.

Caesar cipher is for educational purposes only. Never use it for real security!

## 🧪 TryHackMe Lab Example - The "Secret Message Rescue" Game
Time to put this into practice.

In this game, you're helping a security team that's being monitored on their office Wi-Fi. Attackers are watching everything. The team uses a simple Caesar cipher to communicate safely, and you need to:

    Decrypt secret warnings that were intercepted.
    Encrypt new messages before sending them.

The game uses the Caesar cipher with different shift keys. You'll adjust the key, watch the message change, and submit your answers.

Remember: this is purely educational. Real systems don't use the Caesar cipher because it's laughably weak.   

<div align="center">
  <img src="../../images/caesar-cipher-lab.png" width="500"/>
</div> 


## 🛠️ Practical Skills Developed


## 🧰 Tools Used
- TryHackMe platform  
- Solent University Cybersecurity Coursework  

## 🔐 Security Relevance


## 📌 Lessons Learned
⚠️ 