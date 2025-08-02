
---

## 🛠️ Step-by-Step Guide

### 1️⃣ Create an S3 Bucket for Website Hosting

- Named the bucket: `danielzaws.com`
- Enabled **static website hosting**
- Uploaded `index.html`, `style.css`, and `script.js`
- Made objects publicly readable

📷 `screenshots/s3-hosting.png`

---

### 2️⃣ Set Up Hosted Zone in Route 53

- Created a **hosted zone**: `danielzaws.com`
- Copied **NS records** into Network Solutions DNS settings
- AWS now manages DNS for the domain

📷 `screenshots/route53-zone.png`

---

### 3️⃣ Request an SSL Certificate in ACM

- Requested certificate for `danielzamudioaws.com`
- Chose DNS validation
- Added CNAME record to Route 53
- Certificate status: ✅ Issued

📷 `screenshots/acm-certificate.png`

---

### 4️⃣ Create a CloudFront Distribution

- Origin: S3 Bucket website endpoint  
- Alternate domain name (CNAME): `danielzamudioaws.com`
- Attached the **ACM certificate** for HTTPS
- Forwarded HTTP to HTTPS

📷 `screenshots/cloudfront-settings.png`

---

### 5️⃣ Route Traffic in Route 53

- Created an **A Record (Alias)** to route `danielzamudioaws.com` to CloudFront
- Validated and tested the domain routing

📷 `screenshots/route53-record.png`

---

### 6️⃣ Final Result: Live Interactive Resume

The website is now live at:

🔗 **[https://danielzamudioaws.com](https://danielzamudioaws.com)**

📷 `screenshots/final-site.png`

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

```html
<!-- Resume Website HTML here -->
<!-- See index.html file in repo -->

