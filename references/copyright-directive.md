# Copyright Directive & Photography — Reference Guide

## Last updated: 2025-08-02

## Source
Directive (EU) 2019/790 on Copyright in the Digital Single Market
EUR-Lex: https://eur-lex.europa.eu/eli/dir/2019/790/oj

---

## Table of Contents
1. Overview
2. Art. 3 — Text and Data Mining (Research)
3. Art. 4 — Text and Data Mining (Commercial) + Opt-Out
4. Art. 15 — Press Publishers' Rights
5. Art. 17 — Platform Liability
6. How to Exercise Your Opt-Out Right
7. Relationship with AI Act and Code of Practice

---

## 1. Overview

The Copyright Directive harmonizes copyright rules across the EU, with
specific provisions that affect how photographers' work can be used for
AI training and how platforms handle their content.

For photographers, the most important articles are:
- **Art. 4:** Your right to opt-out of commercial AI training
- **Art. 15:** Press publishers' rights (affects photojournalists)
- **Art. 17:** Platform responsibility for unauthorized use

---

## 2. Art. 3 — TDM for Scientific Research

**What it says:** Research organizations and cultural heritage institutions
may perform text and data mining on works they have lawful access to,
for scientific research purposes.

**Impact on photographers:** Your images CAN be used for non-commercial
academic research without your consent. This exception is mandatory and
cannot be opted out of. However, it is limited to genuine scientific research
by qualifying institutions.

EUR-Lex: https://eur-lex.europa.eu/eli/dir/2019/790/oj#art_3

---

## 3. Art. 4 — Commercial TDM + Opt-Out Right

### What it says (simplified)

**Art. 4(1):** Reproductions and extractions of lawfully accessible works
for text and data mining are allowed.

**Art. 4(3):** UNLESS the rights holder has expressly reserved their rights
"in an appropriate manner." For online content, this means machine-readable
opt-out signals.

### What this means for photographers

You have the legal right to prohibit AI companies from using your photographs
for training their models. But you must actively exercise this right.

### How to opt out

**For images on your website:**
1. Add to your `robots.txt`:
   ```
   User-agent: GPTBot
   Disallow: /

   User-agent: Google-Extended
   Disallow: /

   User-agent: CCBot
   Disallow: /

   User-agent: anthropic-ai
   Disallow: /

   User-agent: Bytespider
   Disallow: /
   ```
2. Add meta tags to pages with images:
   ```html
   <meta name="robots" content="noai, noimageai">
   ```
3. Add HTTP headers:
   ```
   X-Robots-Tag: noai, noimageai
   ```

**For images on stock platforms:**
Each platform has different mechanisms:
- **Adobe Stock:** Opted out of third-party AI training by default since 2023.
  Images may still be used for Adobe's own Firefly model unless further action.
- **Shutterstock:** Has AI training opt-out mechanism in contributor dashboard.
  Also has deals with AI companies — check current contributor agreements.
- **Getty Images:** Has actively litigated against AI companies (Stability AI).
  Provides opt-out mechanisms for contributors.

**In IPTC metadata:**
- Set appropriate rights management fields
- Include explicit copyright notice
- Some propose using IPTC fields to signal opt-out, but this is not yet
  standardized as a universal machine-readable signal

**Limitations of opt-out:**
- Opt-out only applies to FUTURE mining. If your images were already scraped
  before you opted out, there is no retroactive right under Art. 4.
- Enforcement is difficult — there is no universal way to verify compliance
- The GPAI Code of Practice attempts to address this (see Section 7)

EUR-Lex: https://eur-lex.europa.eu/eli/dir/2019/790/oj#art_4

---

## 4. Art. 15 — Press Publishers' Rights

**What it says:** Press publishers have rights over online use of their
press publications by information society service providers.

**Impact on photojournalists:**
- Your photos published in press articles are covered by the publisher's
  neighboring right
- This gives press publishers leverage to negotiate licenses with platforms
  and aggregators
- It does NOT transfer your copyright — you retain authorship rights
- It may affect how your editorial photos are indexed and displayed online

EUR-Lex: https://eur-lex.europa.eu/eli/dir/2019/790/oj#art_15

---

## 5. Art. 17 — Platform Liability (Upload Filters)

**What it says:** Online content-sharing platforms are liable for unauthorized
uploads of copyrighted content unless they:
- Made best efforts to obtain authorization
- Made best efforts to ensure unavailability of notified works
- Acted expeditiously to remove infringing content upon notification

**Impact on photographers:**
- Platforms like Instagram, Facebook, YouTube must take down your images
  if you report unauthorized use
- Some platforms use content recognition tools (similar to YouTube's Content ID)
- You should register your copyright and monitor for unauthorized use
- Platforms cannot claim "safe harbor" as easily as before

EUR-Lex: https://eur-lex.europa.eu/eli/dir/2019/790/oj#art_17

---

## 6. How to Exercise Your Opt-Out Right — Step by Step

### Immediate actions
1. **Update robots.txt** on all your websites (see Art. 4 section above)
2. **Add meta tags** to all pages containing your photographs
3. **Check stock platform settings** and opt out where available
4. **Update IPTC metadata** on all new exports with clear copyright notice

### Formal opt-out letters
For specific AI providers, send a formal opt-out letter:
- Identify yourself as rights holder
- Cite Directive (EU) 2019/790, Art. 4(3)
- Specify the scope (all your works, past and future)
- Request confirmation of compliance
- Set a response deadline

See `assets/templates/opt-out-letter/` for ready-to-use templates.

### Monitoring
- Use reverse image search (Google Images, TinEye) to monitor usage
- Check haveibeentrained.com for presence in known AI datasets
- Monitor C2PA content credentials for unauthorized modifications

---

## 7. Relationship with AI Act and Code of Practice

The Copyright Directive provides the RIGHT to opt out.
The AI Act provides the ENFORCEMENT mechanism.

**AI Act Art. 53(1)(d):** GPAI model providers must comply with EU copyright
law, specifically the opt-out right under Art. 4(3) of the Copyright Directive.

**GPAI Code of Practice (July 2025):**
- Operationalizes how providers must respect opt-outs
- Requires providers to publish copyright policies
- Establishes complaint mechanisms for rights holders
- Sets documentation requirements for training data
- Is a "living document" subject to revision

**Net effect for photographers:**
The legal framework for protecting your images from AI training is in place.
The practical enforcement mechanisms are still maturing. Acting now
(opt-out signals + formal letters + metadata) creates a documented trail
that strengthens your position regardless of how enforcement evolves.
