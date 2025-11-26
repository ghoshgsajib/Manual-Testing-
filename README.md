# 🏦 SecureBank – Complete Manual & Security Testing Project

This repository contains a **complete end-to-end Manual Testing ** for a simulated banking application called **SecureBank**. The aim of this project is to demonstrate strong testing knowledge in both **functional quality assurance**  following **industry standards**, **bank-domain testing processes**, and **OWASP Top 10 security testing techniques**.

This project is ideal for:
- SQA / QA Engineers  
- Fresher QA Job Seekers  
- Manual Testers  
- Security Testers  
- Students preparing portfolios  

---

# 📘 1. Project Introduction

**SecureBank** is an online banking system that allows users to:
- Log in securely  
- Check account balance  
- Transfer funds  
- View transaction history  
- Update profile  
- Request loans  

Banking applications are highly sensitive and require:
- High-level functional testing  
- Deep security testing  
- Strong documentation  

This project includes everything needed for a full SQA portfolio:
- Test Plan  
- Test Scenarios  
- Functional Test Cases  
- Security Test Cases  
- Bug Reports  
- Screenshots  
- Final summary  

---

# 📂 2. Repository Structure

This is the recommended folder structure for your GitHub repo:

<img width="575" height="470" alt="image" src="https://github.com/user-attachments/assets/9a9513a4-87e5-4a72-b6d8-6a525f975c7a" />

# 📝 3. Test Plan (Detailed Overview)

### **3.1 Purpose of Testing**
To ensure that SecureBank:
- Functions correctly  
- Is easy to use  
- Protects user data  
- Is safe from common cyberattacks  

### **3.2 Scope of Testing**
**In-Scope Modules:**
- Login  
- Dashboard  
- Account Balance  
- Fund Transfer  
- Profile Management  
- Transaction History  

**Out-of-Scope:**
- Backend database optimization  
- UI/UX redesign  
- Third-party integrations  

### **3.3 Testing Types Covered**
| Type | Description |
|------|-------------|
| **Functional Testing** | Validates features and workflows. |
| **Usability Testing** | Ensures the UI is easy to use. |
| **Security Testing** | Detects vulnerabilities. |
| **Regression Testing** | Ensures new updates don’t break existing features. |
| **API Testing** | Tests backend logic. |

### **3.4 Entry Criteria**
- Application build deployed  
- Test environment ready  
- Test data prepared  

### **3.5 Exit Criteria**
- 95% functional test cases executed  
- All critical bugs fixed  
- Security vulnerabilities resolved  

### **3.6 Risks**
- Sensitive data exposure  
- Session hijacking  
- Payment failure  

---

# 🧪 4. Test Scenarios (Fully Described)

Below are the high-level scenarios you tested.

### 🔐 **4.1 Authentication Scenarios**
- Login with valid/invalid inputs  
- Forgot password  
- Session timeout validation  
- Check account lock after multiple failed attempts  

### 💳 **4.2 Fund Transfer Scenarios**
- Transfer to same user account  
- Transfer to different bank  
- Validate insufficient balance  
- Cancel transfer  
- Duplicate transfer prevention  

### 👤 **4.3 Profile Management**
- Update email  
- Update phone  
- Change password  
- Upload profile picture  

### 📊 **4.4 Transaction History**
- View last 10 transactions  
- Filter by date range  
- Verify transaction amount and timestamp  

---


# 📋 5. Functional Test Cases (Expanded Table)

## **Functional Test Cases**

| **TC ID**   | **Module** | **Test Case Description**          | **Pre-Condition**       | **Steps**                                                                               | **Expected Result**                    |
| ----------- | ---------- | ---------------------------------- | ----------------------- | --------------------------------------------------------------------------------------- | -------------------------------------- |
| TC_LOGIN_01 | Login      | Login with valid credentials       | User registered         | 1. Open login page <br> 2. Enter valid email <br> 3. Enter password <br> 4. Click Login | User redirected to dashboard           |
| TC_LOGIN_02 | Login      | Login with invalid password        | User registered         | Enter valid email + wrong password                                                      | Error message “Invalid credentials”    |
| TC_BAL_01   | Balance    | Check balance                      | Logged in               | Click **Balance** page                                                                  | System displays correct balance        |
| TC_TRF_03   | Transfer   | Transfer with insufficient balance | Logged in + low balance | Enter a large transfer amount                                                           | Should show **“Insufficient balance”** |
| TC_PROF_02  | Profile    | Change password                    | Logged in               | Enter old + new password                                                                | Password updated successfully          |

---

# 🔐 6. Security Testing (Detailed)

Banking apps must be secure. Below is the security coverage:

## **🛡 6.1 OWASP Top 10 Testing**

| **OWASP Code** | **Vulnerability**                        | **Description**                  |
| -------------- | ---------------------------------------- | -------------------------------- |
| A1             | Broken Access Control                    | Users accessing others’ accounts |
| A2             | Cryptographic Failures                   | Sensitive data not encrypted     |
| A3             | Injection Attacks                        | SQL / XML / Command Injection    |
| A4             | Insecure Design                          | Weak session logic               |
| A5             | Security Misconfiguration                | Exposed debug endpoints          |
| A7             | Identification & Authentication Failures | Weak login policies              |
| A8             | Software & Data Integrity Failures       | Missing integrity checks         |
| A9             | Security Logging Failures                | Missing audit trails             |
| A10            | Server-Side Request Forgery (SSRF)       | Manipulating backend calls       |

---

# 🛡️ 7. Security Test Cases

| **TC ID**   | **Vulnerability**      | **Test Description**               | **Steps**              | **Expected Result**     |
| ----------- | ---------------------- | ---------------------------------- | ---------------------- | ----------------------- |
| SEC_AUTH_01 | Brute Force            | Repeated login attempts            | Try 10 wrong passwords | Account must lock       |
| SEC_SQL_02  | SQL Injection          | Inject `' OR 1=1--`                | Attempt login          | Login should NOT bypass |
| SEC_XSS_03  | Stored XSS             | Insert `<script>alert(1)</script>` | Refresh page           | Script must NOT execute |
| SEC_IDOR_04 | IDOR                   | Unauthorized user access           | Change user ID in URL  | Access denied           |
| SEC_API_05  | Missing Authentication | API call without token             | Remove auth header     | API must reject request |

---

# 🛠️ 8. Tools Used

| **Purpose**             | **Tools**             |
| ----------------------- | --------------------- |
| Test Cases              | Excel                 |
| Test Plan & Summary     | MS Word / Google Docs |
| Bug Tracking (Optional) | Jira / Trello         |

---

Author
Name: Sajib Ghosh
Project: SecureBank Manual & Security Testing 
University: Daffodil International University
