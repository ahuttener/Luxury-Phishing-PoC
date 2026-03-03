

<img width="2739" height="1531" alt="Screenshot 2026-03-03 192401" src="https://github.com/user-attachments/assets/7adf5eb7-b2e9-415c-a2cf-495c1c81f88c" />

```
# Luxury-Phishing-PoC
A Cybersecurity Proof of Concept (PoC) demonstrating high-ticket phishing techniques, social engineering, and local data interception for educational purposes.


# 🛡️ Luxury-Phishing-PoC

This is a **Cybersecurity Awareness** project designed to demonstrate the mechanics of high-ticket phishing attacks. It uses a professional car dealership frontend (**sonasauto.ie**) to illustrate how attackers leverage luxury branding and psychological triggers to harvest user data.

---

### 🎯 Project Objective
The goal of this **Proof of Concept (PoC)** is to educate users and developers on the dangers of **Social Engineering**. It highlights how "basic" data collection (Name, Email, and Phone) can be the starting point for devastating cyberattacks, such as identity theft and account hijacking.

---

### 🧠 The Anatomy of the Attack

#### 1. Pretexting & Psychological Triggers
* **Urgency & Greed:** The site features a high-visibility, pulsing banner: *"⚠ Limited time offer: 0% APR for new applications today!"*. This creates **FOMO (Fear Of Missing Out)**, rushing the user into making decisions without checking security red flags.
* **Professional Trust:** By using a polished, high-end visual identity, the attacker lowers the victim's guard. Users are naturally conditioned to trust professional-looking interfaces.

#### 2. Technical Execution (The Modal Trap)
* **Zero URL Change:** The data capture form opens in a **Modal (pop-up)**. This is a tactical choice: the user stays on the "trusted" homepage, so they don't notice any suspicious redirections in the browser's address bar.
* **Local Interception:** For ethical demonstration purposes, the JavaScript code uses `event.preventDefault()`. The data is intercepted and displayed on the screen only, ensuring it **never leaves the user's browser**.

---

### ⚠️ Why "Basic Data" is a High Risk
Many users believe that sharing just a name, email, and phone number is "low-risk". However, in a real-world scenario, this leads to:

1. **Spear Phishing:** Attackers can call or text the victim by name, pretending to be a bank manager or dealership representative to steal 2FA codes.
2. **SIM Swapping:** Targeted attempts to hijack the victim's phone line by social engineering mobile carriers.
3. **OSINT Correlation:** Using the email and phone to find other leaked credentials in public databases to compromise the victim's primary accounts.

---

### 🚀 How to Run the Demo
1. Clone this repository.
2. Open `index.html` in any modern web browser.
3. Click on the **"Get a Quote"** button or the **"0% APR"** banner.
4. Submit the form to see the **Cybersecurity Awareness Alert** and the link back to this analysis.

---

### ⚖️ Legal Disclaimer
This project is for **educational purposes only**. It was created to promote cybersecurity awareness. Unauthorized use of these techniques for malicious purposes is strictly prohibited and may be illegal.

---

### 🔗 About the Author
Check my full profile and other security projects:
[https://github.com/ahuttener](https://github.com/ahuttener)
