# GEO Readiness Analysis (Generative Engine Optimization)
**Site:** Digital Marketing with AG  
**Current Date:** June 2026  
**Auditor Status:** Pass/Fail GEO compliance review  

---

## 1. GEO Readiness Score: 68/100

### Score Breakdown
- **Citability (18/25%):** Good definitions but lacks high-extraction targets (bolded sentences, summary blockquotes).
- **Structural Readability (15/20%):** Headings are clean, but missing structured comparison tables and lists.
- **Authority & Brand Signals (10/20%):** Weak off-page citation triggers (Wikipedia, Reddit, LinkedIn mentions).
- **Technical Accessibility (18/20%):** XML sitemap active, robots.txt allows standard crawlers. llms.txt is missing.
- **Multi-Modal Content (7/15%):** Images present but missing data charts and tables suitable for LLM summarizers.

---

## 2. Platform Evaluation
- **Google AI Overviews (SGE):** 72/100. Leverages structured JSON-LD schemas well. Needs better on-page lists.
- **ChatGPT Search (SearchGPT):** 65/100. Relies heavily on RSS, sitemaps, and direct web crawling. Brand authority gaps decrease prominence.
- **Perplexity AI:** 68/100. Prefers clear, citation-friendly comparison tables and high-density, authoritative references.

---

## 3. Technical Crawler Access Status
- **Robots.txt Status:** Active, but lacks explicit rules for next-generation search bots.
- **LLMs.txt Status:** ❌ Missing (Needs creation).
- **Sitemap Index:** Registered, but needs inclusion in robots.txt.

---

## 4. Brand Mention Analysis & Gaps
- **Wikipedia:** 0 mentions. *Gap:* Need to build developer/strategic profiles citing AG's marketing models.
- **Reddit:** Low organic discussion. *Gap:* Actively share case study summaries on r/SEO and r/solopreneur.
- **LinkedIn:** Good activity, but lacks structured links back to site articles.
- **YouTube:** Missing video transcriptions linking back to written posts.

---

## 5. Passage-Level Citability of Existing Posts

### Post 1: `seo-geo-aeo-unified-framework.mdx`
- **Passage 1 (Introduction):** 145 words. *Status:* Highly citability-friendly. Explains the transition from keywords to answer extraction.
- **Passage 2 (What is GEO?):** 152 words. *Status:* Good, but needs a bolded definition sentence to trigger direct-answer extraction.

### Post 2: `social-media-automation-ai.mdx`
- **Passage 1 (AI Engagement Engine):** 162 words. *Status:* Strong. Self-contained explanation of n8n scheduling nodes.
- **Passage 2 (Pitfalls):** 115 words. *Status:* Too short for complex RAG synthesis. Needs expansion to ~140 words.

### Post 3: `digital-monetization-strategies.mdx`
- **Passage 1 (E-commerce conversion):** 139 words. *Status:* Self-contained and highly citable.
- **Passage 2 (Stripe integrations):** 172 words. *Status:* Slightly long. Recommend splitting or refining to 150 words.

---

## 6. Top 10 Ranked GEO Improvements

| Rank | Improvement Action | Effort | Impact | Status |
|---|---|---|---|---|
| 1 | Create `robots.txt` allowing ChatGPT/Claude/Perplexity bots | Low | High | Pending |
| 2 | Create `llms.txt` to help AI parsers quickly index key topics | Low | High | Pending |
| 3 | Add FAQPage JSON-LD schema to blog posts | Medium | High | Done (`SEO.astro`) |
| 4 | Embed direct bolded answers under questions | Low | High | Pending |
| 5 | Insert 3 comparison tables mapping SEO vs GEO vs AEO | Medium | High | Pending |
| 6 | Create a dedicated GEO/AEO topic hub page | Medium | Medium | Pending |
| 7 | Expand paragraphs on core topics to 134-167 words | Medium | Medium | Pending |
| 8 | Incorporate citation-rich outbound links | Low | Medium | Pending |
| 9 | Add BreadcrumbList schema | Medium | Medium | Done (`SEO.astro`) |
| 10 | Drive brand mentions on Reddit and industry blogs | High | High | Ongoing |

---

## 7. Action Plan

### Quick Wins (Under 30 Mins)
- Create `robots.txt` at `/public/robots.txt` allowing all AI search bots.
- Create `llms.txt` at `/public/llms.txt` defining website architecture.

### Medium Effort (1-2 Hours)
- Write GEO and AEO pillar posts containing comparison tables and AEO blocks.
- Generate topic page at `/src/pages/topics/geo-aeo.astro`.
- Update blog layout to pass structured breadcrumb arrays to `SEO.astro`.
