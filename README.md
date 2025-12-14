
# AI Data Scientist Handbook 2026
Data science is rapidly evolving so this handbook aims at cutting through the noise and curate the AI-native tools, workflows, and resources that can actually help data scientists work more effectively.

It emphasizes AI-native workflows and agentic analytics, prioritizing tools and resources that align with real data science work. Rather than covering everything, the focus is on cutting through the noise and highlighting what is genuinely useful right now.

If you want to read more about the motivation behind this project, see the [About](#about) section.

## Table of Contents
- [Tools](#tools)
  - [Modern BI & Analytics Tools](#modern-bi--analytics-tools)
  - [Conversational Analytics Tools](#conversational-analytics-tools)
  - [Miscellaneous Tools](#miscellaneous-tools)
- [Foundation Models](#foundation-models)
- [Learning Resources](#learning-resources)
  - [Newsletters](#newsletters)
  - [Courses](#courses)
  - [YouTube Channels](#youtube-channels)
- [Conferences](#conferences)
- [About](#about)

<a id="tools"></a>
## 🛠️ Tools

### Modern BI & Analytics Tools

This section highlights **modern, forward-leaning BI and analytics tools** that go beyond traditional dashboarding.  
The focus is on tools that emphasize semantic layers, metrics-as-code, search-driven analytics, notebooks, and tighter integration with modern data and AI workflows.

Well-known, legacy BI platforms (Looker, PowerBI, Qlik, Tableau) are intentionally excluded to keep this list **high-signal** and oriented toward how analytics is evolving rather than how it has historically been done.

| Tool | Category | What It's Good At | Why It Matters for DS |
|------|----------|-------------------|------------------------|
| [Omni](https://www.omni.co/) | Semantic BI / Metrics Layer | SQL-first BI with strong semantic modeling | Bridges analytics and engineering workflows |
| [Steep](https://www.steep.app/) | Metrics & Analytics | Lightweight, modern metrics exploration | Faster iteration than traditional BI |
| [Lightdash](https://www.lightdash.com/) | Open-source BI | dbt-native BI with metrics-as-code | Fits modern analytics stacks |
| [Evidence](https://evidence.dev/) | Analytics Reporting | Markdown + SQL driven reports | BI as code, versionable insights |
| [Hex](https://hex.tech/) | Notebook BI | Notebooks, dashboards, collaboration; AI-powered conversational analytics | Analyst-to-stakeholder friendly with self-serve AI features |
| [Mode](https://mode.com/) | Analytics Platform | SQL + Python with reporting | Strong hybrid DS / BI workflows |
| [Preset](https://preset.io/) | Open-source BI | Managed Apache Superset | Scalable, customizable BI |
| [Metabase](https://www.metabase.com/) | Open-source BI | Simple querying and dashboards | Fast exploration with low friction |
| [ThoughtSpot](https://www.thoughtspot.com/) | Search-Driven Analytics | Natural language search with AI-assisted insights | Brings search-style analytics to large datasets |

#### Standalone Semantic Layer Tools

Dedicated semantic layer platforms that sit between your data warehouse and consumption tools (BI, AI, applications). They provide a single source of truth for metrics, dimensions, and business logic (decoupled from any specific BI tool).

| Tool | Type | What It's Good At | Why It Matters |
|------|------|-------------------|----------------|
| [Cube](https://cube.dev/) | Open-source / Cloud | Headless semantic layer with REST, GraphQL, MDX, and SQL APIs; caching and pre-aggregations | API-first, works with any BI tool or AI agent; strong for embedded analytics |
| [AtScale](https://www.atscale.com/) | Enterprise | Universal semantic layer with MDX/DAX support; integrates with Power BI, Tableau, Excel | Enterprise-grade; bridges legacy BI tools with modern cloud warehouses |
| [dbt Semantic Layer (MetricFlow)](https://docs.getdbt.com/docs/build/about-metricflow) | Open-source / Cloud | Metrics-as-code defined alongside dbt models; integrates with dbt Cloud | Tight integration with dbt workflows; single place for transforms + metrics |
| [Malloy](https://www.malloydata.dev/) | Open-source | Semantic modeling language from Google; compiles to SQL for BigQuery, Snowflake, Postgres, etc. | Lightweight, expressive; good for teams wanting code-first semantic models |

*If you want to know more about the semantic layer, check out [this article](https://read.futureproofds.com/p/semantic-layers-and-the-future-of-agentic-analytics).*

### Conversational Analytics Tools

Tools that let you talk to your data via conversational AI, natural-language querying, or AI-assisted analytics, but that don't quite fit into the modern BI category.

| Tool | What it does |
| --- | --- |
| [PandasAI](https://pandas-ai.com/) | AI-driven interface for Python dataframes; ask questions and get insights and visuals. |
| [Julius AI](https://julius.ai/) | Conversational AI analyst for data insights and charts (supports spreadsheets/CSV/sheet imports). |
| [Zerve AI](https://www.zerve.ai/) | Conversational interface for querying and exploring data. |
| [DataGPT](https://datagpt.com/) | Conversational AI data analyst that generates insights and deep analysis from business data. |
| [FineChatBI](https://www.fanruan.com/en/finechatbi) | Conversational analytics tool to ask questions and build dashboards and visualizations. |
| [Vanna AI](https://vanna.ai/) | Natural-language chat interface for querying SQL databases; generates SQL and charts/summaries. |
| [Powerdrill (Chat with Database)](https://powerdrill.ai/features/chat-with-database) | Chat-based analytics interface for asking questions and analyzing data without writing SQL. |
| [Wren AI](https://www.getwren.ai/) | Natural-language interface for querying and interacting with data sources. |

### Miscellaneous Tools

This section includes **tools built specifically with data scientists in mind** that don’t fit into the other categories but are still highly relevant to modern, AI-native data science workflows.

| Tool | What it’s for | Why it belongs here |
|------|---------------|---------------------|
| [Google Agent Development Kit (ADK)](https://cloud.google.com/vertex-ai/docs/agent-builder/overview) | Framework for building structured, tool-using agents | Designed for analytical and reasoning-heavy workflows, not just chatbots |
| [MCP Toolbox for Databases](https://github.com/modelcontextprotocol/servers) | Standardized way to connect agents to databases | Directly addresses a core DS need: safe, structured access to data sources |
| [Metaflow](https://metaflow.org/) | DS-first workflow and experiment framework | Built to let data scientists move from notebooks to production without heavy infrastructure |
| [cleanlab](https://cleanlab.ai/) | Data quality and label issue detection | Focuses on a uniquely DS problem: silent data and label errors that hurt model performance |



<a id="foundation-models"></a>
## 🤖 Foundation Models
This section lists foundation models (open-source and commercial) that are relevant to aim at solving core data science problems, including models for tabular data, time series, recommendations, and multimodal analysis.

Use this section as a starting point for exploring foundation models and their capabilities.

| Model | Domain | Organization | Access Type | Primary Use Case |
| --- | --- | --- | --- | --- |
| [TimeGPT](https://www.nixtla.io/) | Time series | Nixtla | API / Open | Forecasting and anomaly detection |
| [TimesFM](https://github.com/google-research/timesfm) | Time series | Google | Open | Zero-shot forecasting |
| [Chronos](https://github.com/amazon-science/chronos-forecasting) | Time series | Amazon AWS | Open | General forecasting |
| [Moirai](https://github.com/SalesforceAIResearch/uni2ts) | Time series | Salesforce | Open | Multi-domain forecasting |
| [Toto](https://github.com/DataDog/toto) | Observability | Datadog | Open | High-cardinality forecasting |
| [MOMENT](https://github.com/moment-timeseries-foundation-model/moment) | Time series | CMU | Open | Multi-task (forecasting, anomaly, etc.) |
| [Granite TTM-R2](https://github.com/ibm-granite/granite-tsfm) | Time series | IBM | Open | Sequential prediction |
| [TabPFN](https://github.com/PriorLabs/TabPFN) | Tabular | Prior Labs | Open | Classification and regression |
| [TableGPT2](https://huggingface.co/tablegpt/TableGPT2-7B) | Tabular / NLP | Zhejiang Univ. | Open | Table question answering and code generation |
| [Netflix RecSys Model](https://netflixtechblog.com/foundation-model-for-personalized-recommendation-1a0bd8e02d39) | Recommendations | Netflix | Proprietary | Personalization at scale |
| [Spotify 2T-HGNN](https://research.atspotify.com/publications/personalized-audiobook-recommendations-at-spotify-through-graph-neural-networks) | Recommendations | Spotify | Proprietary | Cross-modal recommendations |

*If you want to know more about foundation models for data science, check out [this article](https://read.futureproofds.com/p/what-are-foundation-models-and-why-data-scientists-should-care).*

<a id="learning-resources"></a>
## 📚 Learning Resources

This section lists **learning resources** that go beyond generic theory and either align with *AI-native data workflows* or *applied data science with modern AI tools*.

### Newsletters
- [Future Proof Data Science](https://read.futureproofdatascience.com/): A weekly newsletter for data scientists who want to stay relevant and grow their careers in the age of AI (and beyond).
- [Jam with AI](https://jamwithai.substack.com/): A newsletter inspired by real-world AI/ML events & projects
- [To Data & Beyond](https://youssefh.substack.com/): A newsletter for mastering Data Science & AI—Beyond the Basics
- [Daily Dose of Data Science](https://blog.dailydoseofds.com/): A free newsletter for continuous learning about data science and ML, lesser-known techniques, and how to apply them in 2 minutes.
- [Neural Pulse](https://neuralpulse.io/subscribe): A 5-minute, human-curated newsletter delivering the best in AI, ML, and data science (twice a week).


### Courses

| Resource | What It Covers | Why It Belongs Here |
|----------|----------------|---------------------|
| [AI Workflows Bootcamp](https://futureproofds.com/) | A cohort-based program that helps data scientists master AI workflows and automation to 10× productivity, stay relevant, and accelerate their careers. | Built for data scientists, by data scientists. |
| [DeepLearning.AI Courses](https://www.deeplearning.ai/courses/) | AI/ML foundations and applied developer workflows | Useful for DS learners who need *conceptual grounding* alongside applied workflows. |
| [Building AI Agents and Agentic Workflows Specialization (Coursera)](https://www.coursera.org/specializations/building-ai-agents-and-agentic-workflows) | Building and orchestrating agent-based AI systems (LangChain, LangGraph, tool calling) | Focuses on *agentic workflows* that map directly to DS productivity scenarios. |
| [Introduction to LangGraph (LangChain Academy)](https://academy.langchain.com/courses/intro-to-langgraph) | Building stateful, multi-actor agents with LangGraph | Hands-on course for building agentic workflows directly applicable to DS automation. |


### YouTube Channels

- [Data Neighbor Podcast](https://www.youtube.com/@dataneighborpodcast): Hosted by industry veterans Hai Guan, Sravya Madipalli, and Shane Butler, covering data science careers, AI trends, and professional growth.
- [AI Engineer](https://www.youtube.com/@aiDotEngineer): Official channel from the AI Engineer conference/community, featuring talks on AI engineering, agents, and applied AI development.

*Feel free to reach out to me if you have any suggestions for channels that should be added to this list!*


<a id="conferences"></a>
## 🏆 Conferences

### United States

| Conference | Date | Location | Details |
|------------|------|----------|----------|
| [ODSC AI East 2026](https://odsc.ai/east/) | April 28-29, 2026 | Boston, MA | Various tracks including ML, NLP, MLOps, and Data Visualization. 250+ speakers. |
| [ODSC AI West 2026](https://odsc.ai/west/) | OCT 27-29, 2026 | Burlingame, CA | Focuses on AI and data science with workshops, hands-on training, and strategic insights. |
| [IBM Think 2026](https://www.ibm.com/events/think/) | May 4-7, 2026 | Boston, MA | Focuses on AI productivity, trusted data, scalable AI architectures, and cost optimization. |
| [Data + AI Summit 2026](https://www.databricks.com/dataaisummit) | June 15-18, 2026 | San Francisco, CA | Hosted by Databricks. Includes discussions, networking, and hands-on training. |
| [Machine Learning Week 2026](https://machinelearningweek.com/) | May 5-6, 2026 | San Francisco, CA | Focuses on making AI products robust and deployment-worthy. |
| [The AI Conference 2026](https://aiconference.com/) | Sept 30 - Oct 1, 2026 | San Francisco, CA | Vendor-neutral event by the creators of MLconf. Features AI research, engineering, and applied ML. |
| [The Data Science Conference](https://www.thedatascienceconference.com/) | May 28-29, 2026 | Chicago, IL | Vendor-free, sponsor-free, and recruiter-free conference for data science professionals. |
| [AI Engineer World's Fair 2026](https://www.ai.engineer/worldsfair) | June 30 - July 2, 2026 | San Francisco, CA | Largest technical AI conference with 20 tracks, 250 speakers, 6,000+ attendees. |
| [Agentic Analytics Summit](https://cube.dev/events/agentic-analytics-summit-presented-by-cube) | Oct 29, 2025 | Virtual | Presented by Cube. Focuses on agentic systems, semantic layers, and the future of AI-powered analytics. |

### Europe

| Conference | Date | Location | Details |
|------------|------|----------|----------|
| [Data Innovation Summit 2026](https://datainnovationsummit.com/) | May 6-8, 2026 | Stockholm, Sweden | Covers data governance, literacy, machine learning, with speakers from major companies. |
| [ECML PKDD 2026](https://ecmlpkdd.org/2026/) | Sept 7-11, 2026 | Naples, Italy | Premier European conference on machine learning and knowledge discovery in databases. |
| [NeurIPS 2025](https://neurips.cc/) | Nov 30 - Dec 7, 2025 | San Diego, CA, USA | Leading AI/ML research conference. Covers deep learning, AI ethics, and large-scale models. |
| [World AI Cannes Festival 2026](https://www.worldaicannes.com/) | Feb 12-13, 2026 | Cannes, France | Focuses on AI, ML, and data science. Features AI technologies and global innovators. |
| [DATA 2026](https://data.scitevents.org/) | July 16-18, 2026 | Porto, Portugal | International conference on data science, technology, and applications. |
| [AI Engineer Europe 2026](https://www.ai.engineer/europe) | April 8-10, 2026 | London, UK | First official AI Engineer Europe event. Large multitrack technical AI conference for 1000+ AI engineers. |

# Contributing

If you want to add to the repository or find any issues, please feel free to raise a PR and ensure correct placement within the relevant section or category.

# About
This repo exists because data science is entering a new phase.

AI tools are no longer “nice to have” side experiments. They are becoming part of how we actually do the work, from analysis and exploration to production workflows.

As demand grows for data scientists who understand how to integrate AI into their existing workflows, the signal-to-noise ratio is getting worse. There are endless tools, ideas, and opinions, many of them generic or borrowed from other fields.

The goal of this repo is to cut through that noise. It’s a curated set of resources that are either built specifically for data scientists or closely aligned with how we already work. Not an exhaustive list, and not a guide, just a focused snapshot of what’s worth paying attention to right now.

# FAQs
1. **How is curation done?** Curation is based on thorough research, recommendations from people I trust, my 7+ years of experience as a Data Scientist and extensive work integrating AI into data science workflows.
2. **Are all resources free?** Most resources here will be free, but I will also include paid alternatives if they are truly valuable to your career development.
3. **How often is the repository updated?** I plan to come back here as often as possible to ensure all resources are still available and relevant and also to add new ones.

If you have questions or feedback send me a message through [here](https://www.linkedin.com/in/andresvourakis/). Enjoy!
