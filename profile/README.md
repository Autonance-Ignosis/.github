# 🚀 Autonance – Smart Loan Assistance & E-Mandate Platform

Autonance is an intelligent, AI-powered web application that streamlines financial services like **loan applications**, **e-mandate setups**, **KYC verification** . With role-based access for **Customers**, **Banks**, and **Admins**, Autonance ensures a seamless and secure user experience using cutting-edge technologies.

---

## 🏗️ System Architecture

![System Architecture](https://res.cloudinary.com/dte1f5c5z/image/upload/fl_preserve_transparency/v1746703302/system1_you4cf.jpg?_s=public-apps)

---

## 👥 User Roles & Workflow

### 🔹 Customer

1. **Authentication**:  
   Customers sign in using **Google OAuth**.

2. **KYC Verification**:
   - On first login, users must submit **Aadhaar** and **PAN card** images.
   - OCR models (using **Tesseract** and **OpenCV**) extract and validate the information.
   - KYC verification is processed manually by Admins within **1–2 business days**.
   - ML insights assist admins in verifying authenticity.

3. **Chatbot Support**:
   - New users are guided using a chatbot powered by **Mistral LLM**, **FAISS**, and **Sentence Transformers**.

4. **Post-KYC Features**:
   - View **transaction history** from **aggregated customer accounts** with **graph analytics**.
   - Apply for **loans** from any bank (linked or unlinked to their account).
   - **Loan purposes** are customizable.

5. **Loan Approval**:
   - Loan applications are reviewed by the selected **bank**.
   - Evaluated using a **Loan Prediction ANN model** (trained on 2005–2017 dataset) and **user CIBIL score**.

6. **Notifications**:
   - Users receive real-time SMS updates via **Twilio**, powered by **Kafka**-based event-driven architecture.

7. **e-Mandate Setup**:
   - After loan approval, customers must set up an e-mandate with one of their bank accounts.
   - Once approved by the bank:
     - Loan is disbursed.
     - Repayments are auto-deducted on mandate dates.
   - **Warnings** issued for insufficient balance.
   - Banks may take **legal action** after a threshold of missed payments.

---

### 🔹 Bank

- **Loan Application Review**:
  - Approve or reject applications using ML predictions & user credit history.
- **Mandate Validation**:
  - Accept or reject customer mandates.
- **Risk Assessment**:
  - Analyze repayment behavior using aggregated account data.

---

### 🔹 Admin

- **KYC Verification**:
  - Review extracted OCR data.
  - Use ML insights to assist decision-making.
  - Approve or reject verification status.

---

## 💡 Tech Stack

| Layer              | Technology                           |
|-------------------|--------------------------------------|
| **Frontend**       | React                                |
| **Backend**        | Spring Boot, Flask                   |
| **Database**       | PostgreSQL (via NeonDB)              |
| **Authentication** | Google OAuth                         |
| **Event Queue**    | Kafka                                |
| **OCR & KYC**      | Tesseract, OpenCV                    |
| **ML/AI**          | TensorFlow, scikit-learn, Mistral LLM |
| **Notifications**  | WebSocket, Twilio SMS                |

---

## 📈 Features Summary

- 🔐 Google OAuth Authentication  
- 🧠 AI-Powered Chatbot for customer support  
- 📄 Automated KYC with OCR and ML-assisted verification  
- 💳 Aggregated multi-bank transaction history visualization  
- 🧾 Intelligent loan prediction with ANN  
- 🔁 e-Mandate Setup and Auto Payment System  
- 📬 Kafka-based event notifications with Twilio  
- 👮 Admin dashboard for verification and compliance  

---


