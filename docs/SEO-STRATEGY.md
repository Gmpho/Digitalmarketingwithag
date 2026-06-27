# SEO Strategy — Digital Marketing with AG
*Generated: 2026-06-27 | Template: Publisher/Content Blog*

---

## 1. Business Overview

| Field | Detail |
|---|---|
| **Site Name** | Digital Marketing with AG |
| **Domain** | digitalmarkingwithag (Cloudflare Pages) |
| **Type** | Content Publisher / Digital Marketing Blog |
| **Framework** | Astro v7 — static output, Tailwind CSS v4 |
| **Core Topics** | SEO, GEO, AEO, Social Automation, Monetization |
| **Monetization** | Display ads, affiliate marketing, digital products |
| **Target Audience** | Content creators, solopreneurs, indie marketers, bloggers learning AI-era search |

### Mission Statement
To be the most actionable, technically precise resource for understanding SEO, GEO, and AEO in the age of AI-generated search — and to teach readers how to turn organic traffic into passive income.

---

## 2. Current Site Assessment

### Strengths
- ✅ Astro v7 static site — extremely fast, LLM-crawlable HTML output (no JS required)
- ✅ 3 published posts covering all 3 core topics
- ✅ MDX content system with `pubDate`, `title`, `description`, `tags` frontmatter
- ✅ Existing `SEO.astro` component injecting JSON-LD schema + OG tags
- ✅ BlogPosting / WebSite schema already in place
- ✅ Dark mode + responsive design implemented

### Gaps
- ❌ Only 3 published blog posts — insufficient topical authority
- ❌ No author page with credentials (E-E-A-T risk)
- ❌ No `/topics` taxonomy pages
- ❌ No FAQ schema on posts
- ❌ No newsletter / email capture
- ❌ No internal linking strategy implemented
- ❌ About page lacks detailed credentials / author bio
- ❌ No editorial policy or correction policy pages

---

## 3. Target Audience Personas

### Persona 1: "The Indie Content Creator"
- Age 22–35, runs a niche blog or YouTube channel
- Wants to understand why their content doesn't rank
- Questions: "What is GEO?", "How do I get cited by ChatGPT?"
- Entry point: long-tail blog searches, TikTok/Reels referral

### Persona 2: "The Monetization Seeker"
- Experienced blogger (6–24 months) with some traffic
- Wants to add income streams beyond AdSense
- Questions: "How do I use affiliate links properly?", "What digital products can I sell?"
- Entry point: Google search for "how to monetize a blog"

### Persona 3: "The AI-Curious Marketer"
- Works in marketing at an SMB, exploring AI search tools
- Wants practical framework to present to their team
- Questions: "What is the difference between SEO and GEO?", "How do AI Overviews work?"
- Entry point: LinkedIn shares, AI newsletter referrals

---

## 4. KPI Targets

| Metric | Baseline (Now) | 3 Months | 6 Months | 12 Months |
|--------|----------------|----------|----------|-----------|
| Monthly Organic Sessions | ~0 (new) | 500 | 3,000 | 15,000 |
| Indexed Pages | 5 | 20 | 50 | 100+ |
| Keyword Rankings (Top 20) | 0 | 15 | 60 | 200+ |
| Domain Authority (Ahrefs DR) | <5 | 5 | 12 | 25 |
| Email Subscribers | 0 | 50 | 300 | 1,500 |
| AI Citation Rate (Perplexity/ChatGPT) | 0 | 2 posts cited | 10 posts cited | 25+ posts cited |
| Core Web Vitals (LCP) | Target <2.5s | Pass | Pass | Pass |
| Monthly Revenue | $0 | $50 | $300 | $1,500 |

---

## 5. Content Pillars

The site should organize content into **4 core content pillars** — each becoming a topical authority cluster:

| Pillar | URL | Focus |
|---|---|---|
| SEO Fundamentals | `/topics/seo` | On-page SEO, technical SEO, keyword research |
| GEO & AEO | `/topics/geo-aeo` | AI search optimization, LLM citation, schema |
| Social Automation | `/topics/social-automation` | MCP servers, platform bots, scheduling tools |
| Monetization | `/topics/monetization` | Ads, affiliates, digital products, email funnels |

Each pillar page acts as a **hub**: it explains the topic, lists all related posts, and links to the best external resources.

---

## 6. E-E-A-T Strategy

E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) is critical for AI citations.

### Author Page Requirements
- Full name, headshot, and professional bio
- Listed expertise areas (SEO, GEO, AI search, social automation)
- Links to social profiles (LinkedIn, Twitter/X, GitHub)
- `Person` schema with `sameAs` links to social profiles
- List of all articles authored

### Trust Signals to Add
- `/about` — expanded with actual credentials and origin story
- `/editorial-policy` — how content is researched and kept up to date
- Correction notices on updated posts with `dateModified` in schema

---

## 7. Technical SEO Requirements

| Requirement | Status | Priority |
|---|---|---|
| Static HTML output (Astro) | ✅ Done | — |
| JSON-LD schema (BlogPosting, WebSite) | ✅ Done | — |
| Open Graph tags | ✅ Done | — |
| robots.txt | ❓ Verify | High |
| XML Sitemap | ❓ Verify | High |
| Google Search Console verification | ❓ Unknown | High |
| Canonical tags | ❓ Verify | High |
| dateModified in schema | ❌ Missing | Medium |
| FAQ schema on posts | ❌ Missing | High |
| Author Person schema with sameAs | ❌ Missing | High |
| /topics/* pillar pages | ❌ Missing | Medium |
| Core Web Vitals pass (Cloudflare CDN) | ✅ Expected | — |

### AI Search Readiness Checklist
- [x] Server-side rendered HTML (LLMs can crawl without JS)
- [ ] FAQ schema on every post
- [ ] Person schema for author with sameAs
- [ ] Tables and structured data within content
- [ ] Content freshness — dateModified signals recency
- [ ] Quotable bolded sentences in every section (AEO format)

---

## 8. Internal Linking Strategy

Every new blog post must link to:
1. The **pillar page** for its topic (`/topics/seo`, `/topics/geo-aeo`, etc.)
2. At least **2 related posts** within the same pillar
3. At least **1 cross-pillar link** (e.g., a GEO post links to monetization)

---

## 9. Monetization Integration

### Immediate (Month 1–2)
- Add affiliate links to tools mentioned in posts (Amazon Associates, Impact)
- Install Google AdSense or Ezoic for display ads

### Medium-term (Month 3–6)
- Create and sell at least one digital product (e.g., "GEO + AEO Checklist Template")
- Build email list via ConvertKit or Beehiiv — newsletter signup on blog

### Long-term (Month 7–12)
- Launch a course or workshop on "AI-Era Content Strategy"
- Negotiate sponsored posts with SaaS tools (Zernio, MCP server companies)
- Raptive/Mediavine application when hitting 10k+ monthly sessions

---

## 10. Success Criteria

| Phase | Criteria |
|---|---|
| Phase 1 Complete | Sitemap verified, GSC connected, Author page live, robots.txt confirmed |
| Phase 2 Complete | 20+ posts published, 3 topic pillar pages live, first affiliate sale |
| Phase 3 Complete | 3,000+ monthly organic sessions, email list at 300+, 5+ AI citations confirmed |
| Phase 4 Complete | 15,000+ monthly sessions, DA 25+, recurring monthly revenue $1,500+ |
