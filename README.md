# 🤖 AI Customer Support Automation System (Beastlife Assignment)

## 📌 Overview

This project demonstrates an AI-driven customer support automation system that analyzes incoming customer queries, classifies them into predefined categories using AI, and stores structured data for insights and automation.

A working prototype is built using **n8n**, showcasing real-time AI-powered workflow automation integrated with Google Sheets and dashboard analytics.

This system demonstrates how AI can transform customer support from reactive operations to proactive, data-driven decision-making.

---

## 🎯 Objective

* Automatically analyze incoming customer queries
* Classify queries into predefined categories using AI
* Store structured data for analysis
* Generate insights through dashboards
* Enable automation and scalable support workflows

---

## ⚙️ Workflow Architecture

Webhook (Receive Query) → AI Classification (OpenAI) → Structure Data → Google Sheets → (Optional Auto Reply / Automation)

---

## 🧠 AI-Powered Query Classification

The system uses an LLM (OpenAI) to classify queries into the following categories:

* Order Tracking
* Delivery Delay
* Refund Request
* Product Complaint
* Subscription Issue
* Payment Failure
* General Query

### Example

**Input:**

```
My order is not delivered yet
```

**Output:**

```
Delivery Delay
```

---

## 🧪 Live Workflow Example

**Webhook Input:**

```json
{
  "query": "My order is not delivered yet"
}
```

**AI Output:**

```
Delivery Delay
```

**Stored Output (Google Sheets):**

| Query                         | Category       |
| ----------------------------- | -------------- |
| My order is not delivered yet | Delivery Delay |

---

## 🖼 Workflow Diagram

![Workflow Overview](WorkFlow.png)

---

## 🔄 n8n Workflow

The workflow is implemented using **n8n** and includes:

* Webhook node to receive queries
* OpenAI node for classification
* Structured Output Parser for clean JSON response
* Set node to structure data (Query, Category, Timestamp)
* Google Sheets node to store results

📁 **Workflow File:**
`workflow.json` → Contains the complete n8n workflow export for replication

---

## 📊 Dashboard & Insights

### 📌 Issue Distribution

![Issue Distribution](pie.png)

This chart shows the percentage distribution of customer issues:

* ~18.18% → Delivery Delay, Order Tracking, Product Complaint, Refund Request
* ~9.09% → General Query, Payment Failure, Subscription Issue

---

### 📌 Platform-wise Issue Analysis

![Platform Analysis](platform.png)

This chart shows how issues are distributed across platforms (WhatsApp, Email, Website, Instagram).

#### Key Insights:

* WhatsApp has the highest volume of issues
* Website and Email also contribute significantly
* Helps identify platform-specific problem areas

---

### 📌 Trends Over Time

* Every query is stored with a **Timestamp** in Google Sheets
* This enables **weekly and monthly trend analysis**
* Future enhancement: Implementing time-series dashboards (line charts) to visualize weekly/monthly query trends
* Trend data helps predict staffing needs and automation priorities

---

## 📊 Data Storage

Customer queries are stored in **Google Sheets** in structured format:

| Query | Category | Timestamp |
| ----- | -------- | --------- |

This enables:

* Trend analysis (weekly/monthly)
* Dashboard creation
* Automation triggers
* Historical reporting

---

## 📈 Business Insights

* Logistics-related issues (Delivery Delay, Order Tracking) account for ~36% of all queries
* Product complaints and refunds are also major contributors (~36% combined)
* Subscription and payment issues (~18%) can be largely automated
* A significant portion of repetitive queries can be automated using AI, reducing dependency on manual support
* Timestamp data enables identifying peak complaint periods for proactive action

---

## ⚡ Automation Opportunities

* **Order Tracking** → Auto-send tracking link via WhatsApp/Email
* **Delivery Delay** → Notify logistics team automatically
* **Refund Request** → Trigger refund workflow
* **Product Complaint** → Escalate to human support agent
* **General Query** → AI chatbot response via FAQ
* **Payment Issues** → Generate support ticket automatically
* **Subscription Issue** → Auto-check account status and respond
* **Complex/Unresolved Issues** → Auto-escalate to human agent with full context

---

## 📈 Scalability

* Webhook-based architecture supports high query volumes without infrastructure changes
* Cloud AI models (OpenAI) enable real-time classification at scale
* Google Sheets can be replaced with a database (PostgreSQL, Airtable) for larger volumes
* Easily integrates with CRM tools, chatbots, and helpdesk platforms
* Adding new query categories requires only a prompt update — no code changes
* Reduces manual workload significantly as volume grows

---

## 🚀 Future Enhancements

* WhatsApp & Instagram API integration for direct message handling
* Real-time AI chatbot for instant automated responses
* Sentiment analysis to prioritize urgent or angry customers
* Power BI / Looker Studio dashboards for advanced analytics
* Multi-language support for regional customers
* Weekly/monthly trend line charts for volume forecasting

---

## 🛠️ Tech Stack

| Component     | Tool                          |
| ------------- | ----------------------------- |
| AI Model      | OpenAI GPT (gpt-4.1-mini)     |
| Automation    | n8n                           |
| Database      | Google Sheets                 |
| Visualization | Excel (Pivot Tables + Charts) |
| Integration   | Webhooks / REST APIs          |

---

## 🚀 How It Works

1. User sends query via webhook (from WhatsApp, Instagram, Email, or Website)
2. AI model classifies the query into a predefined category
3. Structured data (Query, Category, Timestamp) is generated
4. Data is stored in Google Sheets
5. Dashboard visualizes insights and trends
6. Automation triggers appropriate response or escalation

---

## 📁 Repository Structure

```
├── workflow.json                     → n8n workflow export
├── customer_query_dashboard.xlsx     → Excel dashboard with pivot table and charts
├── WorkFlow.png                      → n8n workflow diagram
├── pie.png                           → Issue distribution chart
├── platform.png                      → Platform-wise analysis chart
└── README.md                         → Project documentation
```

---

## 💡 Conclusion

This project demonstrates how AI + automation can transform customer support by:

* Reducing manual effort through intelligent classification
* Improving response time with automated replies
* Generating actionable business insights from raw query data
* Enabling scalable operations without increasing headcount
* Identifying trends to proactively address recurring issues

---

## 🔗 Author

**Nithin M**
📧 [nithinmgowda06@gmail.com](mailto:nithinmgowda06@gmail.com)
🔗 https://www.linkedin.com/in/nithinm06/
