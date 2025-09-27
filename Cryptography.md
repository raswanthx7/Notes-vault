# Topics Covered
- Cryptography Definition
- How Cryptography Works
- Example in Computers
- Role of Algorithms (RSA, Ed25519)
- What is RSA
- How RSA Works
- Example with GitHub
- RSA vs Ed25519
- Default SSH Key Behavior



---

##  Cryptography = Secret Writing

- **Crypto** = secret / hidden  
- **Graphy** = writing  

So **cryptography** literally means **secret writing** 

---

##  What it does

- Changes normal data (**plain text**) into a **secret code** (**cipher text**)  
- Only the person with the **right key** can decode it back to normal text  

---

##  Example in computers

- Apps like **WhatsApp, SSH, GitHub, banking apps** all use cryptography.  

Algorithms like **RSA** and **Ed25519** are used to:  

- **Encrypt** (lock) your data  
- **Decrypt** (unlock) your data  
- **Authenticate** (prove identity)  

## In short

Cryptography = **science of securing data** so that only the **intended person** can read it.

---

##  What is RSA?

**RSA = Rivest–Shamir–Adleman** (the names of the 3 scientists who invented it).  

- One of the oldest and most widely used encryption algorithms for secure communication.  
- In SSH keygen, RSA is the algorithm that generates your **public/private key pair**.

---

##  How it works

You generate two keys:

- **Private Key (id_rsa)** → stays safe on your system.  
- **Public Key (id_rsa.pub)** → shared with servers (like GitHub, Linux, etc.).  

When you connect:  

- Your system uses the private key to prove identity.  
- The server checks it using the public key.  
-  No password needed, but still very secure.

---

##  Example with GitHub

If you choose RSA, GitHub will accept it like:  

`ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQ...`


- You paste that into **GitHub → Settings → SSH and GPG Keys → New SSH Key**.  
- GitHub then knows: *“Yes, this private key belongs to you.”*

---

##  RSA vs Ed25519

| Feature       | RSA                     | Ed25519                         |
|---------------|------------------------|---------------------------------|
| Age           | Old                    | New                             |
| Key length    | Longer (2048/4096 bits)| Shorter                         |
| Speed         | Slower                 | Faster                          |
| Security      | Strong                 | Stronger at smaller key sizes   |
| Support       | Widely supported       | Modern systems                  |

- GitHub recommends **Ed25519**, but **RSA still works perfectly**.  

---

##  Default SSH Key Behavior

- If you ran `ssh-keygen` **without** `-t ed25519`, it defaulted to RSA keys.  
- That’s why you see files like:  
    - `id_rsa`
    - `id_rsa.pub`

---

## The GitHub-recommended way

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

- Let’s break it down :

    - `-t ed25519` → choose key type = Ed25519 (newer, faster, more secure than RSA).

    - `-C "your_email@example.com"` → add a comment inside the key (usually your GitHub email) so that if you have many keys, you know which one is for what.

    - The result is → files named `id_ed25519` (private) and `id_ed25519.pub` (public).

---
