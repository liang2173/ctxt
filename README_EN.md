# 🧠 AI Memo — Immersive Spaced-Repetition Quiz System

An AI-powered memory reinforcement tool built on cognitive science. Upload your study notes, let AI generate multi-level quiz questions, and let the spaced-repetition algorithm handle your review schedule.

## ✨ Features

- **🤖 AI Question Generation** — Upload `.docx` / `.txt` / text paste; DeepSeek automatically extracts knowledge points and generates multiple-choice, fill-in-the-blank, and short-answer questions
- **🧠 Spaced Repetition** — Improved SM-2 scheduling engine pushes reviews right at the forgetting threshold
- **📈 Multi-Level Progression** — Choice → Fill-in-blank → Short-answer → Mastered, four-tier advancement
- **🔪 Kill & Respawn** — "Kill" mastered items to hide them; auto-respawn after 48 hours for reinforcement
- **📁 Multi-Project Support** — Independent question banks per subject, no cross-contamination
- **🧩 Batched Practice** — 10 knowledge points per batch, unlock progressively to avoid fatigue
- **⭐ Understand-Only & Wrong Book** — Mark low-priority items for quick review; collect mistakes in a dedicated mode for focused practice
- **📡 Live AI Progress** — Streaming output, progress bar, stage indicators, and card-based result preview
- **🔍 Pre-Check Panel** — Free local preview: item count, chunk plan, token estimate, image detection — confirm before spending API credits
- **📥 Auto-Backup** — Automatic `.json` backup download on every import; never lose data to a browser cache clear

## 🚀 Quick Start

1. Download `app.html`
2. Open in browser (Chrome/Edge recommended)
3. Go to Settings → enter your [DeepSeek API Key](https://platform.deepseek.com/)
4. Switch to Bank → upload a knowledge-point document or paste text
5. Click "AI Generate" → wait for completion
6. Switch to Study → start practicing

## 🧪 The Science

AI Memo is built on four well-established findings in cognitive psychology:

- **Ebbinghaus Forgetting Curve (1885)** — We forget ~74% within 24 hours. Spaced review at the forgetting threshold flattens the curve.
- **Testing Effect (Roediger & Karpicke, 2006)** — Active retrieval yields 2–3× better long-term retention than passive re-reading.
- **Desirable Difficulty (Bjork, 1994)** — Moderate challenge during learning enhances long-term memory, even if it feels harder in the moment.
- **Dual Coding Theory (Paivio, 1971)** — Multiple retrieval pathways strengthen recall. AI Memo generates questions from multiple angles for each knowledge point.

## 📖 Usage

### Importing Knowledge Points

Three methods:

- **File Upload** — Drag & drop `.docx` / `.txt` files (PDFs must be text-based; image-based PDFs will be rejected with a warning)
- **Paste Text** — Supports numbered formats (`1、`, `2.`, `一、`, etc.); auto-splits into individual items
- **Manual Import** — For pre-formatted Q&A pairs using `question|answer` syntax

### Study Flow

1. **Choice** — Build basic recognition; advance after 2 consecutive correct answers
2. **Fill-in-blank** — Reinforce key terminology recall
3. **Short-answer** — Train full content reproduction (self-assess with optional appeal)
4. **Kill** — Remove mastered items; auto-respawn after 48 hours

### Data Safety

- All data stored locally in browser LocalStorage
- Automatic `.json` backup download on every AI import
- Manual export/import with multi-project detection (restore all or merge)

## 🛠 Tech Stack

- **Frontend:** HTML5 + CSS3 + Vanilla JavaScript (single-file, zero-dependency)
- **AI Engine:** DeepSeek Chat API with streaming (SSE)
- **Storage:** LocalStorage with automatic legacy-format migration
- **Document Parsing:** Custom ZIP-stream `.docx` parser + pdf.js

## ⚠️ Notes

- Requires a valid DeepSeek API Key
- Single upload recommended up to ~65 items (auto-chunked for larger sets)
- Image-based PDFs (e.g., PPT exports, scans) cannot be processed
- Clearing browser data will delete local data — keep your backup files

## 📄 License

MIT
