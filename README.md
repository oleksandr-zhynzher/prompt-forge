# 🧠 Prompt Forge

> **AI-Powered Learning Companion for Developers**

PromptForge is an intelligent MCP server that acts as a smart proxy between you and AI assistants like Cursor, Claude, or ChatGPT. It captures, analyzes, and transforms your AI interactions into actionable learning insights—all while keeping your data private and secure on your local machine.

---

## 🎯 **Why Prompt Forge?**

As developers, we often rely on AI assistants to solve problems, but we don't always understand the *why* behind the solutions. Prompt Forge bridges this gap by:

- 📊 **Tracking your AI interactions** in real-time
- 🔍 **Identifying knowledge gaps** and learning patterns  
- 📈 **Providing daily insights** to accelerate your growth
- 🔒 **Keeping everything local** - your data never leaves your machine
- 🎓 **Transforming AI dependency** into genuine skill development

---

## ⚡ **Key Features**

### 🔄 **Intelligent Proxy Server**
- Seamless integration with Cursor, VS Code, and other AI tools
- Real-time request/response logging and analysis
- Support for multiple LLM providers (OpenAI, Anthropic, Ollama, etc.)
- Zero-latency passthrough with optional caching

### 🧠 **Smart Analysis Engine**
- **Pattern Recognition**: Detects repetitive questions and knowledge gaps
- **Complexity Scoring**: Measures prompt sophistication over time
- **Context Awareness**: Groups related queries into learning sessions
- **Trend Analysis**: Tracks your learning progression and skill development

### 📊 **Comprehensive Reporting**
- **Daily Learning Summaries**: Markdown reports with insights and recommendations
- **Weekly Progress Reviews**: Trend analysis and skill gap identification
- **Interactive Dashboards**: Real-time metrics and visualizations
- **Export Options**: Integration with Notion, Obsidian, and learning platforms

### 🔒 **Privacy-First Architecture**
- **100% Local Processing**: All data stays on your machine
- **Encrypted Storage**: SQLite database with optional encryption
- **Configurable Retention**: Automatic data cleanup policies
- **Audit Logs**: Complete transparency over data handling

---

## 🛠️ **Technical Architecture**

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   AI Assistant  │    │  Prompt Forge   │    │   LLM Provider  │
│   (Cursor, etc) │◄──►│  Proxy Server   │◄──►│ (OpenAI, etc)   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                                │
                                ▼
                       ┌─────────────────┐
                       │ Analysis Engine │
                       │ • Pattern Detection
                       │ • Knowledge Gaps
                       │ • Learning Insights
                       └─────────────────┘
                                │
                                ▼
                       ┌─────────────────┐
                       │ Local Database  │
                       │ • Encrypted SQLite
                       │ • Prompt History
                       │ • Analysis Results
                       └─────────────────┘
```

### **Core Components**

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Proxy Server** | Node.js + Express | Intercepts and forwards AI requests |
| **Database** | PostgreSQL | Stores prompts, responses, and metadata |
| **Analysis Engine** | Local LLM (Ollama) | Analyzes patterns and generates insights |
| **Report Generator** | React + Markdown/HTML | Creates daily summaries and reports |
| **Web Dashboard** | React | Interactive analytics and configuration |

---

## 🚀 **Getting Started**

### **Prerequisites**
- Node.js 18+ 
- Ollama (for local analysis)
- Your favorite AI assistant (Cursor, VS Code, etc.)

### **Quick Installation**

```bash
# Clone the repository
git clone https://github.com/yourusername/prompt-forge.git
cd prompt-forge

# Install dependencies
npm install

# Initialize the database
npm run setup

# Start the server
npm start
```

### **Configuration**

Create a `.env` file in the root directory:

```env
# Server Configuration
PORT=3000
HOST=localhost

# Database
DATABASE_URL=./data/prompt-forge.db
ENCRYPTION_KEY=your-secure-key-here

# LLM Providers
OPENAI_API_KEY=your-openai-key
ANTHROPIC_API_KEY=your-anthropic-key
OLLAMA_HOST=http://localhost:11434

# Analysis Settings
ANALYSIS_MODEL=mistral:7b
REPORT_FREQUENCY=daily
RETENTION_DAYS=30
```

### **Cursor Integration**

1. Open Cursor Settings
2. Navigate to "AI Providers" 
3. Add custom endpoint: `http://localhost:3000/v1/chat/completions`
4. Set your API key as usual - Prompt Forge will forward it securely

---

## 📊 **Example Output**

### **Daily Learning Report**

```markdown
# 📈 Daily Learning Summary - March 15, 2024

## 🎯 **Session Overview**
- **Total Prompts**: 23
- **Unique Topics**: 8
- **Learning Sessions**: 4
- **Complexity Score**: 7.2/10 (↑ 0.8 from yesterday)

## 🔍 **Knowledge Gaps Identified**
1. **TypeScript Generics** (5 related prompts)
   - You seem uncertain about constraint syntax
   - Suggestion: Review conditional types and mapped types

2. **Angular Testing** (3 related prompts)
   - MockProvider setup appears challenging
   - Suggestion: Practice TestBed configuration

## 💡 **Learning Recommendations**
- [ ] **Quick Win**: TypeScript utility types (15 min)
- [ ] **Deep Dive**: Angular testing patterns (1 hour)
- [ ] **Explore**: RxJS error handling strategies

## 📊 **Progress Metrics**
- **Questions per hour**: 2.3 (optimal: 1-3)
- **Follow-up rate**: 67% (shows good engagement)
- **Understanding score**: 8.1/10 (based on clarification frequency)
```

---

## 🗺️ **Implementation Roadmap**

### **Step 1: Core Proxy Server**
- [x] Express.js server setup
- [x] PostgreSQL database schema
- [x] Basic request/response logging
- [ ] OpenAI API compatibility layer
- [ ] Request forwarding with headers

### **Step 2: Data Storage & Security**
- [ ] Database models for prompts/responses
- [ ] Data encryption at rest
- [ ] Configurable data retention policies
- [ ] Basic audit logging

### **Step 3: Analysis Engine**
- [ ] Ollama integration for local LLM
- [ ] Simple pattern detection algorithms
- [ ] Knowledge gap identification
- [ ] Session grouping and context awareness

### **Step 4: Report Generation**
- [ ] Daily summary generation
- [ ] React-based report interface
- [ ] Markdown export functionality
- [ ] Basic learning recommendations

### **Step 5: Web Dashboard**
- [ ] React dashboard setup
- [ ] Real-time metrics display
- [ ] Interactive charts and visualizations
- [ ] Configuration management UI

### **Step 6: Cursor Integration**
- [ ] Proxy endpoint for Cursor
- [ ] API key forwarding
- [ ] Error handling and logging
- [ ] Connection testing tools

### **Step 7: Advanced Analytics**
- [ ] Learning progression tracking
- [ ] Complexity scoring algorithms
- [ ] Trend analysis over time
- [ ] Personalized recommendations

### **Step 8: Export & Integrations**
- [ ] Multiple export formats (PDF, HTML, Markdown)
- [ ] Notion workspace integration
- [ ] Email/Slack notifications
- [ ] Custom report templates

### **Step 9: Team Features**
- [ ] Multi-user support
- [ ] Shared team dashboards
- [ ] Collaborative learning goals
- [ ] Team knowledge gap analysis

### **Step 10: Plugin System**
- [ ] Plugin architecture design
- [ ] Custom analyzer plugins
- [ ] Third-party integration APIs
- [ ] Plugin marketplace foundation

---

## 🎯 **Identified Improvements**

Based on the initial concept, here are key enhancements we're implementing:

### **1. Enhanced Privacy & Security**
- **End-to-end encryption** for all stored data
- **Configurable data retention** policies
- **Audit trails** for all data access
- **Air-gapped mode** for maximum privacy

### **2. Advanced Analytics**
- **Machine learning models** for pattern recognition
- **Contextual understanding** of code and concepts
- **Skill progression tracking** over time
- **Predictive recommendations** for learning paths

### **3. Extensible Architecture**
- **Plugin system** for custom analyzers
- **API-first design** for third-party integrations
- **Modular components** for easy maintenance
- **Docker containerization** for easy deployment

### **4. Better User Experience**
- **Real-time insights** as you code
- **Smart notifications** for learning opportunities
- **Gamification elements** to encourage growth
- **Mobile companion app** for on-the-go insights

### **5. Collaboration Features**
- **Team dashboards** for shared learning
- **Knowledge sharing** within organizations
- **Mentorship matching** based on skills
- **Peer learning recommendations**

---

## 🤝 **Contributing**

We welcome contributions! Here's how you can help:

1. **🐛 Bug Reports**: Found an issue? Open a GitHub issue
2. **💡 Feature Requests**: Have an idea? Let's discuss it
3. **🔧 Code Contributions**: Check our contributing guidelines
4. **📖 Documentation**: Help improve our docs
5. **🧪 Testing**: Help us test new features

### **Development Setup**

```bash
# Clone and setup
git clone https://github.com/yourusername/prompt-forge.git
cd prompt-forge
npm install

# Run in development mode
npm run dev

# Run tests
npm test

# Build for production
npm run build
```

---

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 **Acknowledgments**

- **Cursor Team** for inspiring the proxy architecture
- **Ollama Project** for making local LLMs accessible
- **OpenAI** for pioneering conversational AI
- **The Developer Community** for valuable feedback and ideas

---

**Made with ❤️ for developers who want to learn, not just copy-paste.**

*"The best way to learn from AI is to understand what you don't know."*
