# 🚀 Automated LinkedIn AI Content & Publishing Engine

**Author:** Hakob Nahapetyan  
**Links:** [LinkedIn](https://www.linkedin.com/in/hakob-nahapetyan) | [Data Analytics Certifications](https://www.credly.com/badges/99e76b98-bb99-4d0a-8692-19defd59171d/public_url)  

An autonomous end-to-end publishing pipeline built with **Make.com**, leveraging **Perplexity AI** for real-time web research, **OpenAI (GPT-4o & DALL-E 3)** for copywriting and image synthesis, and the **LinkedIn API** for zero-touch content distribution.

---

## 📸 Scenario Architecture

<p align="center">
  <img src="assets/scenario_diagram.png" width="95%" alt="Make.com Scenario Pipeline" />
</p>

---

## 🔄 End-to-End Workflow & Module Breakdown

1. **Trigger — Slack (`Watch Public Channel Messages`):**
   * Listens for new seed prompts, links, or topic ideas dropped into a designated Slack channel.
2. **Research & Grounding — Perplexity AI (`Create a Chat Completion`):**
   * Searches live web data to synthesize fresh insights, facts, and statistics related to the seed topic.
3. **Flow Control — Router:**
   * Directs data streams and prepares payloads for multi-stage content generation.
4. **Copywriting — OpenAI Assistant (`Message an Assistant`):**
   * Generates formatted, engagement-optimized LinkedIn copy using predefined hook structures, value points, and dynamic hashtags.
5. **Visual Asset Creation — OpenAI (`Generate Images`):**
   * Uses DALL-E to generate a custom 1:1 or 4:5 visual matching the post concept.
6. **File Retrieval — HTTP (`Get a File`):**
   * Downloads the raw image stream from the generated image URL into a binary buffer.
7. **Distribution — LinkedIn (`Create a User Image Post`):**
   * Registers the media upload and publishes the finalized post and visual directly to the personal profile feed.

---

## ⚙️ Tech Stack & Integrations

* **Workflow Orchestration:** Make.com
* **Research Agent:** Perplexity AI API
* **Language & Vision Models:** OpenAI Assistant API & DALL-E 3
* **Communication & Ingestion:** Slack API
* **Social Distribution:** LinkedIn REST / Graph API

---

## 📥 How to Import the Blueprint

1. Clone or download `blueprints/linkedin_auto_posts_blueprint.json` from this repository.
2. Log in to [Make.com](https://www.make.com) and create a **New Scenario**.
3. Click the **`...` (More)** menu at the bottom toolbar.
4. Select **Import Blueprint** and select the JSON file.
5. Map your respective Slack, OpenAI, Perplexity, and LinkedIn connection credentials.