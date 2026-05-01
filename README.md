# 🌺 Sanae Siam — Cultural AI Guide for Thailand
### HACK4 SuperAI Season 4 Submission

> *"Sanae" (เสน่ห์) — The Thai word for charm, allure, and enchantment.*  
> *Sanae Siam bridges the invisible gap between foreign visitors and Thai cultural nuance.*

---

## 🏆 Project Overview

**Sanae Siam** is a premium AI-powered cultural travel web application designed for foreign tourists visiting Thailand. Unlike generic travel apps, Sanae Siam goes beyond logistics — it provides **culturally nuanced, context-aware guidance** covering destinations, food, traditions, heritage, and etiquette.

The core insight: **Most travel apps tell you *where* to go. Sanae Siam tells you *how* to be there.**

### The Problem
Foreign tourists in Thailand frequently make unintentional cultural mistakes — entering temples incorrectly dressed, mishandling food customs, accidentally violating laws (lèse-majesté, vaping ban) — due to a lack of accessible, specific, and culturally sensitive information.

### The Solution
A 5-step agentic AI pipeline that:
1. Researches cultural context in real-time
2. Classifies user intent and sensitivity level
3. Personalizes responses by nationality, religion, dietary needs
4. Synthesizes verified Thai government + community data
5. Delivers warm, specific, actionable guidance in English

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🗺 **Kingdom Map** | 29 curated Thai destinations across 6 regions with cultural context |
| 🎭 **Soul / Heritage** | Living Heritage, Sacred Architecture, Muay Thai, performing arts |
| 🍜 **Gastronomy** | 10 signature dishes with allergen flags, dietary tags, spice levels |
| 🙏 **Respect / Etiquette** | 8 cultural conduct categories with do/don't guidance |
| 🤖 **Thai AI Advisor** | Real-time Claude-powered chat with cultural nuance system prompt |
| 🎪 **Traditions** | 6 major Thai festivals and rituals with sensitivity ratings |

---

## 🧠 AI Architecture

```
User Query
    │
    ▼
Intent Classifier
(destination / food / etiquette / general)
    │
    ├──► Knowledge Base (RAG)
    │    └── TAT API + กรมศิลปากร + Wongnai + data.go.th
    │
    ├──► Real-time Web Search (fallback)
    │    └── Anthropic Web Search Tool
    │
    ▼
Claude Sonnet (claude-sonnet-4-20250514)
+ Cultural Nuance System Prompt
    │
    ▼
Context-Aware Response
(personalized by: nationality, religion, dietary, location)
```

### Why RAG over Fine-tuning?
- ✅ No GPU required — serverless friendly
- ✅ Update knowledge instantly (no retraining)
- ✅ Lower cost — pay per query, not per training run
- ✅ Verifiable sources — cite TAT, government data

---

## 🗃 Data Sources

### Destinations & Places
| Source | Type | Coverage |
|--------|------|----------|
| [TAT Data API](https://tatdataapi.io) | Free API | Attractions, Events, Routes, Hotels |
| [กรมศิลปากร GIS](https://data.go.th) | Open Data | Ancient sites, Museums, Heritage monuments |
| Google Places API | Paid API | Hours, Photos, Real-time status |
| Wikipedia TH/EN | Free API | Cultural background, History |

### Food & Gastronomy
| Source | Type | Coverage |
|--------|------|----------|
| [Wongnai Data Services](https://business.wongnai.com) | B2B API | 260,000+ restaurants, 16M+ reviews |
| [Wongnai NLP Corpus](https://github.com/wongnai/wongnai-corpus) | Open Source | 500K food words, Thai food dictionary |
| [thai-food-open-data](https://github.com/thangman22/thai-food-open-data) | Open Source | Thai dish vocabulary in JSON |
| กรมส่งเสริมวัฒนธรรม | Official | Regional heritage food |

### Culture & Etiquette
| Source | Type | Coverage |
|--------|------|----------|
| [data.go.th](https://data.go.th) | Free API | All government open data |
| สำนักพระพุทธศาสนาแห่งชาติ | Official | Temple rules, Monk etiquette |
| สถานทูตไทย (MFA) | Official | Etiquette guides for foreigners |
| ราชกิจจานุเบกษา | Official | Laws: lèse-majesté, vaping, drugs |
| Reddit r/ThailandTourism | Community | Real traveler Q&A, edge cases |
| Pantip.com | Community | Thai community perspective |

### Real-time Layer
| Source | Coverage |
|--------|----------|
| TAT Events API | Festivals, ceremonies, events calendar |
| กรมอุตุนิยมวิทยา API | Weather, monsoon, seasonal alerts |
| Anthropic Web Search Tool | Breaking news, new regulations |
| User Feedback Loop | Continuous improvement from in-app corrections |

---

## 🗺 Destination Coverage

**29 locations across 22 provinces and 6 regions:**

| Region | Provinces |
|--------|-----------|
| Central | Bangkok, Ayutthaya, Nakhon Pathom, Lopburi, Samut Songkhram |
| North | Chiang Mai, Nan, Mae Hong Son |
| Northeast | Nakhon Ratchasima, Ubon Ratchathani, Roi Et |
| West | Kanchanaburi, Ratchaburi, Phetchaburi, Prachuap Khiri Khan, Sangkhlaburi |
| East | Trat, Chonburi, Rayong |
| South | Nakhon Si Thammarat, Phuket, Krabi |

---

## 🛠 Tech Stack

```
Frontend
├── HTML5 / CSS3 / Vanilla JavaScript
├── Google Fonts — Cormorant Garamond + Montserrat
└── Single-file architecture (no framework dependency)

AI Layer
├── Claude Sonnet (claude-sonnet-4-20250514) via Anthropic API
├── RAG Pipeline — Vector embeddings + Knowledge Base
└── 5-step Agentic Workflow

Data
├── JSON knowledge base (destinations, food, etiquette, traditions)
├── TAT Open Data API
└── data.go.th Government Open Data

Design System
├── Cream editorial palette (#f5f0e8)
├── Terracotta accent (#8b4a2a)
└── Luxury editorial aesthetic — Kinfolk × Condé Nast Traveler
```

---

## 🚀 Setup & Running

### Prerequisites
- A modern web browser (Chrome, Safari, Firefox)
- Anthropic API key ([get one here](https://console.anthropic.com))

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/Sanae_SIAM_HACK4_SuperAI.git

# Navigate to project
cd Sanae_SIAM_HACK4_SuperAI

# Open in browser (no build step needed)
open index.html
```

### Enabling the Thai AI Advisor
1. Open the app in your browser
2. Click **"THAI AI ADVISOR"** in the top navigation
3. Enter your Anthropic API key in the field at the top of the panel
4. Start asking questions about Thai culture, destinations, and food

> **Note:** Your API key is used client-side only and never stored or transmitted to any server other than Anthropic's API directly.

### File Structure
```
Sanae_SIAM_HACK4_SuperAI/
├── index.html          # Main application (single file)
├── data/
│   ├── destinations.json   # 29 Thai destinations
│   ├── dishes.json         # 10 signature dishes
│   ├── traditions.json     # 6 festivals & traditions
│   ├── etiquette.json      # 8 conduct categories
│   └── provinces.json      # 22 provinces + Google Maps links
├── prompts/
│   └── system-prompt.md    # Thai Cultural AI system instruction
└── README.md
```

---

## 🤖 AI System Prompt Design

The Thai AI Advisor uses a carefully engineered system prompt covering:

- **Role definition** — warm local expert, not a tour brochure
- **5 knowledge domains** — destinations, food, etiquette, festivals, laws
- **Sensitivity framework** — Critical / High / Medium / Low with legal warnings
- **Structured output** — JSON schema for UI rendering + human response
- **Personalization** — adapts to user's religion, nationality, dietary needs
- **Anti-patterns** — explicit rules against generic answers and cultural errors

See [`prompts/system-prompt.md`](prompts/system-prompt.md) for the full prompt.

---

## 🎯 What Makes Sanae Siam Different

| Generic Travel App | Sanae Siam |
|-------------------|------------|
| "Wear appropriate clothing" | "Cover shoulders and knees. No flip-flops. Remove shoes at the entrance." |
| Lists tourist spots | Explains cultural significance + do/don't at each place |
| One-size-fits-all answers | Personalized by religion, gender, dietary needs |
| Static content | Real-time research via agentic pipeline |
| English only | Context-aware for international audiences |
| No legal guidance | Covers lèse-majesté, vaping ban, drug laws explicitly |

---

## 📊 Sensitivity Classification System

```
🔴 CRITICAL  — Legal consequences (monarchy, drugs, vaping)
🟠 HIGH      — Strong cultural violation (monks, Buddha images, head)
🟡 MEDIUM    — Cultural faux pas (feet, shoes, public affection)
🟢 LOW       — Good-to-know etiquette (wai, dining customs)
```

---

## 🌏 Expandability

Sanae Siam is designed as a **Thailand-first, world-ready** platform. The same architecture can expand to:

- 🇯🇵 Japan — Onsen rules, bowing etiquette, shrine customs
- 🇮🇳 India — Temple dress, sacred cow, regional food diversity  
- 🇸🇦 Middle East — Halal requirements, Ramadan conduct, dress codes
- 🇻🇳 Vietnam — Ancestor worship, temple etiquette, food culture

Only the **knowledge base changes** — the AI pipeline, RAG architecture, and sensitivity framework remain identical.

---

## 👥 Team & Contributing

Built for **SuperAI Season 4 — HACK4 Hackathon**

### How to Contribute
1. Fork the repository
2. Add destinations to `data/destinations.json` following the existing schema
3. Verify cultural information against official Thai government sources
4. Submit a Pull Request with source citations

### Data Schema for New Destinations
```json
{
  "id": "province-name",
  "name": "Province Name",
  "region": "Central|North|Northeast|East|West|South",
  "image": "https://...",
  "poeticDescription": "One evocative sentence",
  "pills": ["Tag1", "Tag2", "Tag3"],
  "dressCode": ["Rule 1", "Rule 2"],
  "customs": ["Custom 1", "Custom 2"],
  "activities": ["Activity 1", "Activity 2"],
  "googleMapsUrl": "https://maps.app.goo.gl/...",
  "quote": "Poetic closing quote."
}
```

---

## ⚠️ Important Notes

- **Legal Content:** Information about Thai laws (lèse-majesté, drug regulations) is provided for traveler safety. Always verify current regulations with official sources.
- **API Keys:** Never commit your Anthropic API key to the repository. Use environment variables or client-side input as implemented.
- **Cultural Sensitivity:** All cultural content has been cross-referenced with official Thai government sources and community validation.

---

## 📄 License

MIT License — Free to use, modify, and distribute with attribution.

---

<div align="center">

**Sanae Siam** — *เสน่ห์สยาม*

Built with ❤️ for SuperAI Season 4 · HACK4

*Helping the world experience Thailand with grace, understanding, and respect.*

</div>
