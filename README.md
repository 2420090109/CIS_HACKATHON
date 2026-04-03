# 🚀 Cloud-Native API Monitoring & Health Tool

An automated, serverless infrastructure monitoring tool built on **AWS** and hosted via **GitHub Pages**. This project demonstrates a fully decoupled Cloud Infrastructure Services (CIS) architecture.

## 🌐 Live Demo
[Click here to view the Live Tool](https://2420090109.github.io/CIS_HACKATHON/)

---

## 🏗️ System Architecture
This project follows the **AWS Well-Architected Framework** for scalability and cost-optimization:

1.  **Frontend:** HTML5/JavaScript (Bootstrap 5) hosted on **GitHub Pages**.
2.  **API Layer:** **AWS API Gateway** (HTTP API) handling CORS and routing.
3.  **Compute:** **AWS Lambda** (Python 3.12) performing serverless request execution.
4.  **Database:** **Amazon DynamoDB** (NoSQL) for persistent test history logging.



---

## ✨ Key Features
* **Real-Time Latency Analysis:** High-precision measurement of API response times in milliseconds ($ms$).
* **Automated Health Checks:** Categorizes endpoints as "Healthy" or "Unhealthy" based on HTTP status codes.
* **Persistent Audit Trail:** Every test is automatically logged into a NoSQL database for reliability auditing.
* **Serverless Execution:** Zero infrastructure management; scales automatically to handle burst traffic.

---

## 🛠️ Tech Stack
* **Cloud:** Amazon Web Services (Lambda, API Gateway, DynamoDB, IAM).
* **Frontend:** JavaScript (Fetch API), Bootstrap 5.
* **Backend Language:** Python 3.12.
* **Deployment:** GitHub Actions & Pages.

---

## 🚧 Challenges & Resolutions
* **CORS Policy:** Resolved "Preflight" handshake errors by configuring specific Access-Control headers in API Gateway.
* **Type Incompatibility:** Overcame DynamoDB float limitations by implementing the Python `decimal` library for latency recording.
* **Least Privilege Security:** Implemented IAM Roles to ensure the Lambda function only has specific write access to the required database table.

---

## 👨‍💻 How to Use
1. Enter any REST API URL in the input field.
2. Click **Run Test**.
3. View the real-time latency and raw JSON response data.
4. Verify the recorded entry in the **AWS DynamoDB Console**.
