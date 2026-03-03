


<img width="2715" height="1470" alt="phishing" src="https://github.com/user-attachments/assets/c5186af9-da5d-4bc4-840a-69e88b6663b7" />

```
# 🛡️ Luxury-Phishing-PoC

**A Cybersecurity Proof of Concept (PoC) demonstrating high-ticket phishing techniques, social engineering, and local data interception for educational purposes.**

---

![Luxury Car Phishing Simulation](https://github.com/user-attachments/assets/da61066c-1845-42f0-a077-e6f7596b6d17)

### 🎯 Project Objective
The goal of this **Proof of Concept (PoC)** is to educate users and developers on the dangers of **Social Engineering**. It illustrates how attackers leverage professional design and psychological triggers to harvest user data, and how a simple script can intercept sensitive information.

---

### 🧠 How the Phishing is Executed (Technical Flow)

To understand how this attack works, we can break it down into four technical stages:

#### 1. The Lure (Pretexting)
The attack begins with a high-visibility, pulsing banner: *"⚠ Limited time offer: 0% APR for new applications today!"*. This creates **FOMO (Fear Of Missing Out)**, forcing the victim to act quickly and ignore security red flags.

#### 2. The Hook (Modal Interception)
Instead of a separate page, the form opens in a **Modal (pop-up)**. This keeps the user on the "trusted" homepage, so they don't notice any suspicious redirections in the browser's address bar.

#### 3. The Capture (DOM Manipulation)
When the user clicks "Apply Now", the script performs the following actions:
* **Interception:** Uses `event.preventDefault()` to stop the data from being sent to a legitimate server.
* **Harvesting:** Accesses the values typed in the `input` fields (Name, Email, Phone) using the Document Object Model (DOM).

```javascript
// Technical snippet of the capture mechanism
document.getElementById('phishingForm').addEventListener('submit', function(e) {
    e.preventDefault(); // This stops the real form submission
    const capturedName = document.getElementById('nameInput').value;
    const capturedEmail = document.getElementById('emailInput').value;
    const capturedPhone = document.getElementById('phoneInput').value;
    // In a real attack, this data would be sent to an attacker's database here.
}); ```

4. The Illusion
In a real attack, after capturing the data, the victim is usually redirected to a legitimate page to avoid suspicion. In this PoC, we show a Security Awareness Alert to reveal the intercepted data.

⚠️ Why "Basic Data" is a High Risk
Sharing just a name, email, and phone number is enough for:

Spear Phishing: Personalized attacks via WhatsApp/Email using the victim's name to steal 2FA codes.

SIM Swapping: Hijacking the victim's phone line by social engineering mobile carriers.

OSINT Correlation: Finding other leaked credentials in public databases to compromise primary accounts.
```

![7ffebc79-a9fd-4cf2-8e26-c0230632fbde](https://github.com/user-attachments/assets/a1cf6dd8-0e23-4366-adba-9af22328d02b)



🚀 How to Run the Demo
Clone this repository: https://github.com/ahuttener/Luxury-Phishing-PoC

Open index.html in any browser.

Click on the "0% APR" banner.

Submit the form to see the technical analysis.

⚖️ Legal Disclaimer
This project is for educational purposes only. Unauthorized use for malicious purposes is strictly prohibited.

🔗 Project & Author Links
Repository: https://github.com/ahuttener/Luxury-Phishing-PoC

Author Profile: https://github.com/ahuttener

