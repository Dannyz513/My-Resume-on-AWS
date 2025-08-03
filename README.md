
---

![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/188af12e8eb1548fff2d4504e2141da2cf0934f8/diagram-export-8-2-2025-1_27_15-PM.png)


## 🛠️ Step-by-Step Guide

### 1️⃣ Create an S3 Bucket for Website Hosting

- Named the bucket: `danielzamudioaws.com`
- Enabled **static website hosting**
- Uploaded `index.html`, `style.css`, and `script.js`
- Made objects publicly readable

📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/caa7e6511c6d061cff1389e750188b662a1dd86a/S3%20static%20website.png) 

---

### 2️⃣ Set Up Hosted Zone in Route 53

- Created a **hosted zone**: `danielzamudioaws.com`
- Copied **NS records** into GoDaddy DNS settings
- AWS now manages DNS for the domain

📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/800b015adfd85433491c3559c0c774f1d16cec5c/Route%2053.png) 

---

### 3️⃣ Request an SSL Certificate in ACM

- Requested certificate for `danielzamudioaws.com`
- Chose DNS validation
- Added CNAME record to Route 53
- Certificate status: ✅ Issued

📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/cc1724c8fd0a6028d84b135b3ffb318fe687ff0a/ACM.png)

---

### 4️⃣ Create a CloudFront Distribution

- Origin: S3 Bucket website endpoint  
- Alternate domain name (CNAME): `danielzamudioaws.com`
- Attached the **ACM certificate** for HTTPS
- Forwarded HTTP to HTTPS

📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/ccbc9491dfdf3b5ffbf47907a0390be0533ac380/Cloudfront%20D.png)

---

### 5️⃣ Route Traffic in Route 53

- Created an **A Record (Alias)** to route `danielzamudioaws.com` to CloudFront
- Validated and tested the domain routing

📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/d8db6dec7530aa76d1ffba6f886a97101cfa299e/Route%2053%20A%20name.png)

---

### 6️⃣ Final Result: Live Interactive Resume



📷 ![image alt](https://github.com/Dannyz513/My-Resume-on-AWS/blob/e942d8f5e6e1d1589ad8b4da267ef63b4f9c8d89/Final%20resume.png)

---

## 🧠 Key Skills Demonstrated

- 🔒 Configuring SSL/TLS (HTTPS) with ACM
- 🌐 DNS and domain routing with Route 53
- ☁️ Hosting and securing a static site on AWS
- 📉 Cloud cost awareness (no EC2 or backend server used)
- 📦 End-to-end deployment from scratch

---

## 📜 Source Code

### `index.html`

[Open Index Page](https://github.com/Dannyz513/My-Resume-on-AWS/blob/406bb7bdc2f1ba3bf4e024312feee05fb3d32b1a/index.html) 

