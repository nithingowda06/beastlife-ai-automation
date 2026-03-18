# 🤖 AI Customer Support Automation System (Beastlife Assignment)

## 📌 Overview

This project demonstrates an AI-driven customer support automation system designed to analyze customer queries, classify issues, and store structured data for insights and automation. This project includes a working prototype built using n8n to simulate real-time AI-powered customer support automation.

---

## 🎯 Objective

* Automatically analyze incoming customer queries
* Classify queries into predefined categories
* Store structured data for analysis
* Enable automation and dashboard insights

---

## ⚙️ Workflow Architecture

Webhook (Receive Query) → AI Classification (OpenAI) → Structure Data → Google Sheets → (Optional Auto Reply)

---

## 🧠 AI-Powered Query Classification

The system uses an LLM (OpenAI) to classify queries into:

* Order Tracking
* Delivery Delay
* Refund Request
* Product Complaint
* Subscription Issue
* Payment Failure
* General Query

### Example:

**Input:**
My order is not delivered yet

**Output:**
Delivery Delay

---

## 🧪 Live Workflow Example

**Input (Webhook Request):**

```json
{
  "query": "My order is not delivered yet"
}
```

**AI Output:**
Delivery Delay

**Stored in Google Sheets:**

| Query                         | Category       |
| ----------------------------- | -------------- |
| My order is not delivered yet | Delivery Delay |

---

## 🖼 Workflow Diagram

![Workflow Overview](WorkFlow.png)

* n8n workflow
* AI classification node
* Google Sheets output
* Dashboard chart

---

## 🔄 n8n Workflow

* Webhook node to receive queries
* OpenAI node for classification
* Set node to structure data
* Google Sheets node to store results

---

## 📊 Data Storage

Customer queries are stored in structured format in Google Sheets and used for dashboard visualization and trend analysis.

---

## 📈 Insights & Use Case

* Order Tracking, Delivery Delay, Refund Requests, and Product Complaints each contribute ~20%
* Payment Failures and General Queries contribute ~10%

**Key Insight:**
Logistics and product quality are the major areas requiring improvement, while repetitive queries can be automated using AI.

---

## ⚡ Automation Opportunities

* Order Tracking → Auto-send tracking link
* Delivery Delay → Notify logistics team
* Refund Request → Auto-send refund process
* Product Complaint → Escalate to support team
* General Query → AI chatbot response
* Payment Issues → Generate support ticket

---

## 📈 Scalability

* Handles large query volumes via webhook-based architecture
* Uses cloud AI models for real-time classification
* Easily integrates with CRM and support tools
* Supports scalable automation without increasing manual effort

---

## 🚀 Future Enhancements

* WhatsApp & Instagram API integration
* Real-time AI chatbot
* Sentiment analysis for priority handling
* Power BI / Looker Studio dashboards
* Multi-language support

---

## 🛠️ Tech Stack

* AI Model: OpenAI GPT
* Automation: n8n
* Database: Google Sheets
* Dashboard: Excel (Pivot + Pie Chart)
* Integration: Webhooks / APIs

---

## 🚀 How It Works

1. User sends query via webhook
2. AI classifies the query
3. Data is structured and stored
4. Dashboard generates insights
5. Automation triggers responses

---

## 💡 Conclusion

This system demonstrates how AI and automation can improve customer support by reducing manual work, improving response time, generating insights, and scaling operations efficiently.

---

## 🔗 Author

**Nithin M**
📧 [nithinmgowda06@gmail.com](mailto:nithinmgowda06@gmail.com)
🔗 https://www.linkedin.com/in/nithinm06/
