# N8N Automated Email Management System

A comprehensive n8n workflow system for automatically managing customer emails with AI-powered responses, sentiment analysis, and Excel logging.

## 🎯 Features

- **Automatic Email Detection** - Monitors unread emails every 5 minutes
- **AI-Powered Analysis** - Classifies emails by intent and sentiment
- **Smart Response Generation** - Creates professional, contextual replies
- **Thread Management** - Handles multi-turn conversations seamlessly
- **Excel Logging** - Tracks all interactions for auditing
- **Thread Reply Monitoring** - Detects and responds to follow-ups

## 📋 System Architecture

### Workflow 1: Main Email Processor (5-minute intervals)
- Detects unread customer emails
- Analyzes content and classifies intent
- Generates professional AI responses
- Sends replies and marks emails as read
- Logs interactions to Excel

### Workflow 2: Thread Reply Monitor (10-minute intervals)
- Monitors existing email threads
- Detects new unread replies
- Retrieves conversation history
- Sends contextual follow-up responses
- Updates Excel records

## 📁 Files Included

- `workflow-1-main-email-processor.json` - Primary email processing workflow
- `workflow-2-thread-reply-monitor.json` - Thread monitoring workflow
- `email-analysis-prompt.md` - AI prompt for email classification
- `response-generation-rules.md` - Guidelines for AI responses
- `excel-logging-schema.md` - Excel column documentation
- `setup-guide.md` - Installation and configuration instructions

## 🚀 Quick Start

1. **Import Workflows** into n8n
2. **Configure Gmail** API credentials
3. **Set up AI Provider** (Claude or OpenAI)
4. **Create Excel Sheet** for logging
5. **Test** with sample emails

## 📊 Email Categories

- Product Complaint
- Product Change Request
- Appreciation/Positive Feedback
- Product Quality Concern
- Shipping/Delivery Issue
- Refund/Return Request
- Information Inquiry
- Follow-up/Reminder
- Urgent Escalation
- General Customer Support
- Unknown/Other

## 🔧 Requirements

- n8n instance (self-hosted or cloud)
- Gmail API access
- OpenAI or Anthropic API key
- Google Sheets or Excel online
- Basic n8n workflow knowledge

## 📝 License

MIT

## 👤 Author

naqoosh2016

---

For detailed setup instructions, see `setup-guide.md`
