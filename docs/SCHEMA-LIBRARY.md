# Schema Library & JSON-LD Implementation Guide
**Site:** Digital Marketing with AG  
**Author:** AG  
**Scope:** Homepage, Blog Posts, Topic Hubs, About Page, Editorial Policies  

This document serves as the implementation guide and reference library for all structured data schemas across the website. The schemas are fully compliant with Google Rich Results requirements.

---

## 1. Blog Post Schema (BlogPosting + FAQPage + BreadcrumbList)
*Target URL:* `/blog/[slug]`  
*Purpose:* Identifies the page as an article, provides extraction FAQs, and sets hierarchical navigation signals.

### JSON-LD Template (Astro Dynamic Syntax)
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "BlogPosting",
      "@id": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}#article`}",
      "isPartOf": {
        "@type": "WebPage",
        "@id": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}`}",
        "url": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}`}",
        "name": "{title}"
      },
      "headline": "{title}",
      "description": "{description}",
      "image": "{`https://digitalmarkingwithag.pages.dev${image}`}",
      "datePublished": "{pubDate.toISOString()}",
      "dateModified": "{dateModified ? dateModified.toISOString() : pubDate.toISOString()}",
      "author": {
        "@type": "Person",
        "name": "Digital Marketing with AG",
        "url": "https://digitalmarkingwithag.pages.dev/about"
      },
      "publisher": {
        "@type": "Organization",
        "name": "Digital Marketing with AG",
        "url": "https://digitalmarkingwithag.pages.dev",
        "logo": {
          "@type": "ImageObject",
          "url": "https://digitalmarkingwithag.pages.dev/favicon.svg"
        }
      },
      "mainEntityOfPage": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}`}"
    },
    {
      "@type": "FAQPage",
      "@id": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}#faq`}",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is Generative Engine Optimization (GEO)?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Generative Engine Optimization (GEO) is the process of optimizing content to ensure it is selected, cited, and referenced by LLM-based search engines like ChatGPT and Perplexity."
          }
        },
        {
          "@type": "Question",
          "name": "How does GEO differ from traditional SEO?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Unlike traditional SEO, which focuses on keyword position in link lists, GEO optimizes text structure, semantic relevance, and tables for retrieval-augmented generation models."
          }
        }
      ]
    },
    {
      "@type": "BreadcrumbList",
      "@id": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}#breadcrumb`}",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://digitalmarkingwithag.pages.dev"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Blog",
          "item": "https://digitalmarkingwithag.pages.dev/blog"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "{title}",
          "item": "{`https://digitalmarkingwithag.pages.dev/blog/${slug}`}"
        }
      ]
    }
  ]
}
</script>
```

### Checks & Testing
- **Required Fields:** `headline`, `image`, `datePublished`, `author.name`, `publisher.name`, `publisher.logo`.
- **Recommended Fields:** `dateModified` (helps AI bots prioritize updated/fresh content).
- **Validation:** Test on the [Google Rich Results Test Tool](https://search.google.com/test/rich-results) after deployment.

---

## 2. Homepage Schema (WebSite + Organization + SiteLinksSearchBox)
*Target URL:* `/`  
*Purpose:* Establishes brand entity identity, social links, and enabling instant search box integrations.

### JSON-LD Template
```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://digitalmarkingwithag.pages.dev/#organization",
      "name": "Digital Marketing with AG",
      "url": "https://digitalmarkingwithag.pages.dev",
      "logo": "https://digitalmarkingwithag.pages.dev/favicon.svg",
      "description": "Strategies on SEO, GEO, AEO, and marketing automation.",
      "sameAs": [
        "https://www.linkedin.com/in/giftmpho",
        "https://twitter.com/digitalmarkingag",
        "https://github.com/giftmpho"
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://digitalmarkingwithag.pages.dev/#website",
      "url": "https://digitalmarkingwithag.pages.dev",
      "name": "Digital Marketing with AG",
      "publisher": {
        "@id": "https://digitalmarkingwithag.pages.dev/#organization"
      },
      "potentialAction": {
        "@type": "SearchAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://digitalmarkingwithag.pages.dev/search?q={search_term_string}"
        },
        "query-input": "required name=search_term_string"
      }
    }
  ]
}
```

---

## 3. Topic Hub Schema (CollectionPage + ItemList + BreadcrumbList)
*Target URL:* `/topics/geo-aeo`  
*Purpose:* Organizes multiple related posts into a single category index for semantic hierarchy mapping.

### JSON-LD Template
```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "CollectionPage",
      "@id": "https://digitalmarkingwithag.pages.dev/topics/geo-aeo",
      "url": "https://digitalmarkingwithag.pages.dev/topics/geo-aeo",
      "name": "GEO & AEO Guide: AI Search Optimization",
      "description": "A curated collection of resources on Generative Engine Optimization and Answer Engine Optimization."
    },
    {
      "@type": "ItemList",
      "@id": "https://digitalmarkingwithag.pages.dev/topics/geo-aeo/#itemlist",
      "name": "Featured AI Search Articles",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "url": "https://digitalmarkingwithag.pages.dev/blog/seo-geo-aeo-unified-framework",
          "name": "SEO, GEO & AEO: The Unified Visibility Framework for 2026"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "url": "https://digitalmarkingwithag.pages.dev/blog/what-is-generative-engine-optimization",
          "name": "What Is Generative Engine Optimization (GEO)? A Complete 2026 Guide"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "url": "https://digitalmarkingwithag.pages.dev/blog/what-is-answer-engine-optimization",
          "name": "What Is Answer Engine Optimization (AEO)? The 2026 Guide"
        }
      ]
    },
    {
      "@type": "BreadcrumbList",
      "@id": "https://digitalmarkingwithag.pages.dev/topics/geo-aeo/#breadcrumb",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://digitalmarkingwithag.pages.dev"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Topics",
          "item": "https://digitalmarkingwithag.pages.dev/topics"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "GEO & AEO",
          "item": "https://digitalmarkingwithag.pages.dev/topics/geo-aeo"
        }
      ]
    }
  ]
}
```

---

## 4. About Page Schema (Person + ProfilePage)
*Target URL:* `/about`  
*Purpose:* Establishes creator credentials, topical expertise nodes (knowsAbout), and background credibility.

### JSON-LD Template
```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "ProfilePage",
      "@id": "https://digitalmarkingwithag.pages.dev/about/#profile",
      "url": "https://digitalmarkingwithag.pages.dev/about",
      "mainEntity": {
        "@type": "Person",
        "@id": "https://digitalmarkingwithag.pages.dev/about/#person",
        "name": "AG",
        "jobTitle": "Digital Marketing Strategist",
        "url": "https://digitalmarkingwithag.pages.dev/about",
        "image": "https://digitalmarkingwithag.pages.dev/avatar.jpg",
        "knowsAbout": [
          "Search Engine Optimization",
          "Generative Engine Optimization",
          "Answer Engine Optimization",
          "Marketing Automation",
          "Static Web Development"
        ],
        "sameAs": [
          "https://www.linkedin.com/in/giftmpho",
          "https://twitter.com/digitalmarkingag"
        ]
      }
    }
  ]
}
```

---

## 5. Editorial Policy Page Schema (WebPage)
*Target URL:* `/editorial-policy`  
*Purpose:* Signals content integrity, review guidelines, and editorial oversight parameters to Google's quality assessors and LLM spiders.

### JSON-LD Template
```json
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "url": "https://digitalmarkingwithag.pages.dev/editorial-policy",
  "name": "Editorial Policy & Content Guidelines",
  "about": {
    "@type": "Organization",
    "name": "Digital Marketing with AG"
  },
  "mainEntity": {
    "@type": "WebPageElement",
    "name": "Editorial Standards",
    "text": "All content on Digital Marketing with AG is reviewed for technical accuracy, empirical correctness, and readability. AI-generated text undergoes rigorous human validation and editing before publication."
  }
}
```
