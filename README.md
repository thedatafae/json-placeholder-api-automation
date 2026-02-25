# 🚀 Blog API Automation Suite

This repository contains a professional API testing suite developed to validate the core functionalities of a blog management system. The project demonstrates advanced SQA skills including **API Chaining**, **Negative Testing**, and **CI/CD-ready Reporting**.

## 📊 Test Execution Summary
* **Total Requests:** 6
* **Assertions:** 6
* **Pass Rate:** 100% ✅
* **Avg Response Time:** 666ms



## 🛠️ Testing Scenarios
| Scenario | Method | Validation Logic |
| :--- | :--- | :--- |
| **Smoke Test** | `GET` | Verifies system uptime and initial data load (200 OK). |
| **Resource Creation**| `POST`| Creates a new post and **extracts the ID** for chaining. (201 Created). |
| **Data Update** | `PUT` | Validates modification of existing resources (200 OK). |
| **Negative Validation**| `PUT` | Tests server-side behavior on broken payloads (missing title). |
| **Integration/Cleanup**| `DELETE`| Automatically removes the resource created during the POST step. |
| **Resource Absence** | `GET` | Validates 404 response for non-existent IDs (ID: 9999). |

## ⚙️ Technical Highlights
* **API Chaining:** Used JavaScript in the `Tests` tab to capture `jsonData.id` and pass it to the `DELETE` request via environment variables.
* **Environment Separation:** Utilized `{{baseUrl}}` variables to ensure the collection is environment-agnostic.
* **Automated Reporting:** Integrated with **Newman** and **htmlextra** to generate stakeholder-ready dashboards.

## 🚀 How to Run
1. Install Newman: `npm install -g newman newman-reporter-htmlextra`
2. Run the suite:
   ```bash
   newman run collections/No_Auth_API_Project.json -e environments/env.json -r htmlextra




