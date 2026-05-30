````markdown
# N8N Automated Email Management & Lead Generation System

A comprehensive n8n workflow system for automated email management with AI-powered responses AND lead generation with business research automation.

## 🎯 Features

### Email Management (Workflows 1-2)
- **Automatic Email Detection** - Monitors unread emails every 5 minutes
- **AI-Powered Analysis** - Classifies emails by intent and sentiment
- **Smart Response Generation** - Creates professional, contextual replies
- **Thread Management** - Handles multi-turn conversations seamlessly
- **Excel Logging** - Tracks all interactions for auditing
- **Thread Reply Monitoring** - Detects and responds to follow-ups

### Lead Generation & Business Research (Workflow 3 - NEW!)
- **Google Maps Search** - Find businesses by keyword and location
- **Web Search Enrichment** - Extract contact information automatically
- **Website Scraping** - Capture emails and phone numbers from websites
- **LinkedIn Verification** - Verify companies and find decision makers
- **Priority Scoring** - Rank leads on quality (0-100 scale)
- **Google Sheets Export** - Auto-save results to spreadsheet
- **Email Reports** - Get completion reports via email

---

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

### Workflow 3: Lead Generation & Business Research (On-demand or Scheduled)
- Searches for businesses using Google Maps API
- Enriches data with web search and scraping
- Extracts contact details (emails, phones)
- Calculates quality scores (0-100)
- Exports to Google Sheets
- Sends summary reports

---

## 📁 Files Included

### Email Automation
- `workflow-1-main-email-processor.json` - Primary email processing workflow
- `workflow-2-thread-reply-monitor.json` - Thread monitoring workflow
- `email-analysis-prompt.md` - AI prompt for email classification
- `response-generation-rules.md` - Guidelines for AI responses
- `excel-logging-schema.md` - Excel column documentation
- `setup-guide.md` - Installation and configuration instructions

### Lead Generation (NEW)
- `workflow-3-lead-generation.json` - **Complete lead generation workflow**
- `lead-generation-setup.md` - **Setup and configuration guide**
- `lead-generation-nodes.md` - **Detailed node configuration**
- `lead-generation-code-snippets.js` - **Reusable JavaScript functions**
- `lead-generation-env-example` - **Environment variables template**
- `LEAD-GENERATION-QUICK-START.md` - **Quick start summary**

---

## 🚀 Quick Start

### Email Automation
1. **Import Workflows** into n8n
2. **Configure Gmail** API credentials
3. **Set up AI Provider** (Claude or OpenAI)
4. **Create Excel Sheet** for logging
5. **Test** with sample emails

For detailed setup, see [`setup-guide.md`](./setup-guide.md)

### Lead Generation (NEW!)
1. **Import Workflow** `workflow-3-lead-generation.json` into n8n
2. **Set up API keys** (Google Maps, SerpAPI)
3. **Configure Google Sheets** for results storage
4. **Set up Email** for reports
5. **Trigger workflow** with search parameters

For detailed setup, see [`lead-generation-setup.md`](./lead-generation-setup.md)

For quick start checklist, see [`LEAD-GENERATION-QUICK-START.md`](./LEAD-GENERATION-QUICK-START.md)

---

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

---

## 🔍 Lead Generation Examples

### Example 1: Restaurant Search (San Francisco)
```json
{
  "keyword": "michelin star restaurants",
  "location": "San Francisco, CA",
  "radius": 10000,
  "type": "restaurant",
  "max_results": 20
}
```

### Example 2: B2B SaaS Companies (New York)
```json
{
  "keyword": "b2b saas software companies",
  "location": "New York, NY",
  "radius": 5000,
  "type": "company",
  "max_results": 20
}
```

### Example 3: Fitness Centers (Los Angeles)
```json
{
  "keyword": "gym fitness centers",
  "location": "Los Angeles, CA",
  "radius": 3000,
  "type": "gym",
  "max_results": 20
}
```

---

## 📈 Lead Priority Scoring

Leads ranked 0-100:
- **80-100 (Critical):** Hot leads with complete information
- **60-79 (High):** Good leads with most details available
- **40-59 (Medium):** Fair leads needing some research
- **Below 40 (Low):** Incomplete leads requiring more work

---

## 🔧 Requirements

### Email Automation
- n8n instance (self-hosted or cloud)
- Gmail API access
- OpenAI or Anthropic API key
- Google Sheets or Excel online
- Basic n8n workflow knowledge

### Lead Generation
- n8n v1.0+ (self-hosted or cloud)
- Google Maps API key
- Google Sheets API credentials
- SerpAPI key (web search)
- LinkedIn API (optional)
- Gmail credentials (for reports)

---

## 📊 System Performance

| Workflow | Execution Time | Frequency | Data Points |
|----------|----------------|-----------|-------------|
| Email Processor | 30-60 sec/email | Every 5 min | 20+ fields |
| Thread Monitor | 20-40 sec/thread | Every 10 min | Thread history |
| Lead Generation | 45-60 sec/lead | On-demand | 15+ fields |

---

## 🛠️ API Keys Needed

| API | Purpose | Plan | Cost |
|-----|---------|------|------|
| Google Maps | Business search | Places API | Free: 1000/day |
| SerpAPI | Web search | Any plan | $5-50/month |
| Google Sheets | Results storage | Standard | Free |
| LinkedIn | Company data | Varies | Varies |
| OpenAI/Claude | Email AI | Any plan | ~$20/month |
| Gmail | Email access | Standard | Free |

---

## 🔐 Security

- API keys stored in n8n credentials (encrypted)
- Environment variables for sensitive data
- HTTPS/TLS for all communications
- IP whitelisting available
- No data stored locally
- Add `.env` to `.gitignore`

---

## 📚 Documentation

| Document | Purpose |
|----------|---------|
| `setup-guide.md` | Email automation setup |
| `lead-generation-setup.md` | Lead generation setup |
| `lead-generation-nodes.md` | Node configuration reference |
| `lead-generation-code-snippets.js` | Reusable JavaScript functions |
| `lead-generation-env-example` | Environment variables template |
| `LEAD-GENERATION-QUICK-START.md` | Quick start checklist |

---

## 🎯 Use Cases

### Email Automation
- Customer support automation
- Sales inquiry handling
- Complaint resolution
- Lead nurturing
- Follow-up automation

### Lead Generation
- Sales prospecting
- Market research
- Competitor analysis
- Local business outreach
- Industry intelligence gathering

---

## 🛠️ Advanced Features

### Email Automation
- Sentiment analysis of emails
- Multi-language support
- Attachment processing
- Calendar integration
- CRM synchronization

### Lead Generation
- Duplicate detection
- Geographic filtering
- Industry segmentation
- Real-time webhooks
- Custom scoring formulas
- Batch processing
- CRM integration

---

## 📤 Export Options

Results can be exported to:
- Google Sheets (native integration)
- Excel/CSV files
- JSON format
- Webhook notifications (real-time)
- Email reports (automated)
- Database (PostgreSQL, MongoDB)

---

## 🐛 Troubleshooting

### Common Issues

| Issue | Cause | Solution |
|-------|-------|----------|
| "Invalid API Key" | Wrong credentials | Verify in n8n settings |
| No emails extracted | Website blocking scraper | Try email finder API |
| Rate limit exceeded | Too many API calls | Add delays between requests |
| Sheet quota exceeded | Too many appends | Batch updates (10 rows/call) |
| LinkedIn 403 error | Auth token expired | Regenerate access token |

**Detailed troubleshooting:** 
- Email issues: See `setup-guide.md`
- Lead generation issues: See `lead-generation-setup.md`

---

## 📚 Learning Resources

- [n8n Documentation](https://docs.n8n.io/)
- [Google Maps API Docs](https://developers.google.com/maps/documentation)
- [SerpAPI Documentation](https://serpapi.com/docs)
- [n8n Community Forum](https://community.n8n.io/)
- [n8n YouTube Channel](https://www.youtube.com/channel/UCJJCbYRYyVjUDxp6EeKU8vw)

---

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

## 📄 License

MIT

---

## 👤 Author

naqoosh2016

---

## 🙌 Acknowledgments

Built with:
- [n8n](https://n8n.io/) - Workflow automation platform
- [Google Maps API](https://developers.google.com/maps) - Location search
- [SerpAPI](https://serpapi.com/) - Web search
- [OpenAI](https://openai.com/) - AI responses
- [Anthropic Claude](https://www.anthropic.com/) - AI analysis

---

## 🎓 Next Steps

1. **Choose your workflow:**
   - Email automation? Start with `setup-guide.md`
   - Lead generation? Start with `LEAD-GENERATION-QUICK-START.md`

2. **Set up API credentials**
   - Get required keys from API providers
   - Add to n8n credentials

3. **Import and configure**
   - Import workflow JSON into n8n
   - Configure your settings
   - Test with sample data

4. **Deploy**
   - Set up scheduling if needed
   - Configure notifications
   - Monitor logs

---

## 📞 Support

For questions or issues:
1. Check the relevant documentation file
2. Review the troubleshooting section
3. Check n8n community forum
4. Create an issue on GitHub

---

**Last Updated:** 2026-05-30  
**Latest Version:** 2.0 (Added Lead Generation)  
**Compatibility:** n8n v1.0+  
**Status:** ✅ Production Ready  

---

## 📦 What's Included

✅ 3 Complete n8n workflows  
✅ Email automation (2 workflows)  
✅ Lead generation (1 workflow)  
✅ Google Maps integration  
✅ Web search enrichment  
✅ Website scraping  
✅ Contact extraction  
✅ LinkedIn verification  
✅ Priority scoring  
✅ Google Sheets export  
✅ Email reporting  
✅ 6 comprehensive guides  
✅ Reusable code snippets  
✅ Configuration templates  

---

**Ready to automate your workflows?** Start with the Quick Start guides! 🚀
````
