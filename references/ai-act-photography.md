# AI Act & Photography — Reference Guide

## Last updated: 2025-08-02 (Code of Practice entry into force)

## Source
Regulation (EU) 2024/1689 — Artificial Intelligence Act
EUR-Lex: https://eur-lex.europa.eu/eli/reg/2024/1689/oj

---

## Table of Contents
1. Overview and Timeline
2. Art. 50 — Transparency for AI-Generated Content
3. Art. 53-55 — General-Purpose AI Model Obligations
4. Annex III — High-Risk Systems (Biometrics)
5. Recitals Relevant to Photography
6. Practical Scenarios for Photographers

---

## 1. Overview and Timeline

The AI Act entered into force on 1 August 2024. Key compliance dates:

- **2 Feb 2025:** Prohibited AI practices ban applies
- **2 Aug 2025:** GPAI model obligations apply (Art. 53-55); Code of Practice in force
- **2 Aug 2026:** Most remaining provisions apply, including Art. 50 transparency
- **2 Aug 2027:** High-risk AI system obligations for Annex III systems

**For photographers:** Art. 50 transparency obligations formally apply from
August 2026, but the Code of Practice (in force Aug 2025) already sets
practical expectations. Early compliance is recommended.

---

## 2. Art. 50 — Transparency for AI-Generated Content

### What the law says (simplified)

**Art. 50(2):** Providers of AI systems that generate synthetic audio, image,
video, or text content must ensure the output is marked in a machine-readable
format as AI-generated. This means the software provider (Adobe, Google, etc.)
must embed metadata — not the photographer.

**Art. 50(4):** Deployers (= users who publish AI-generated content) must
disclose that the content has been artificially generated or manipulated,
when they make it publicly available.

### Exceptions (critical for photographers)

**Art. 50(4) exceptions:**
- Content that undergoes **human editorial review** where a natural person
  holds editorial responsibility → disclosure obligation is reduced
  (but machine-readable labeling still required)
- Content that is **manifestly artistic, creative, satirical, or fictional**
  → labeling must not hamper the artistic experience, but machine-readable
  marking is still required
- Content used for **law enforcement or national security** → exempt

### What this means for photographers

| Scenario | Provider obligation (Adobe etc.) | Your obligation |
|----------|--------------------------------|-----------------|
| You use AI Denoise | None (not generative) | None |
| You use Generative Remove (small object) | Adobe embeds C2PA metadata | Grey area — recommended to preserve metadata |
| You use Generative Expand significantly | Adobe embeds C2PA metadata | Disclose when publishing publicly; inform commercial clients |
| You generate a full image with Midjourney | Provider must mark output | Full disclosure when publishing; must be machine-readable labeled |
| You do AI-assisted editing on a journalistic photo | Adobe embeds metadata | Full disclosure mandatory — editorial integrity |

### EUR-Lex link
Art. 50: https://eur-lex.europa.eu/eli/reg/2024/1689/oj#art_50

---

## 3. Art. 53-55 — General-Purpose AI Models

These articles apply to AI **providers** (OpenAI, Google, Stability AI, Adobe),
not to photographers directly. However, they matter because:

- **Art. 53(1)(d):** GPAI providers must have a policy to comply with EU copyright
  law, in particular Art. 4(3) of Directive 2019/790 (the opt-out right).
  This is the legal basis for photographers to demand removal from training data.

- **Art. 53(1)(b-c):** Providers must document training data and make summaries
  publicly available. This helps photographers check if their work was used.

### GPAI Code of Practice (July 2025)
The Code of Practice implements Art. 53-55 with practical requirements:
- Providers must publish a copyright policy
- Providers must offer a complaint mechanism for rights holders
- Providers must document dataset sources
- Compliance with opt-out must be demonstrable

See `references/code-of-practice.md` for details.

---

## 4. Annex III — High-Risk (Biometrics)

**Annex III, Category 1:** AI systems for real-time and post remote biometric
identification of natural persons are classified as **high-risk**.

**Impact on photographers:** If you use AI-powered facial recognition to sort,
tag, or identify people in your photos (e.g., Lightroom's People view,
Google Photos face clustering), be aware:

- These are generally **on-device** systems and typically fall under the
  "personal use" exemption
- However, if used **commercially** to identify individuals (e.g., event
  photography matching faces to attendee databases), high-risk classification
  may apply
- **Real-time biometric identification in public spaces** is banned in the EU
  with narrow exceptions (Art. 5)

Most photographers are NOT affected by Annex III, but event/corporate
photographers using facial recognition matching should be aware.

---

## 5. Relevant Recitals

**Recital 133:** Clarifies that transparency obligations under Art. 50 apply
to content that is "deep fakes" — images that "appreciably resemble existing
persons, objects, places, or other entities or events and would falsely appear
to a person to be authentic or truthful." Minor AI edits that don't create
false impressions are less clearly covered.

**Recital 134:** The artistic/creative exception acknowledges that labeling
should not undermine creative freedom, but emphasizes that machine-readable
marking should still be present to allow downstream detection.

---

## 6. Practical Scenarios

### Wedding photographer — Low concern
Uses AI Denoise, AI Masks for editing. Occasionally removes a trash can
with Generative Remove. Posts on Instagram and delivers to clients.
- **Disclosure:** Not legally required for minor generative edits
- **Recommended:** Keep C2PA metadata intact, set IPTC Digital Source Type
- **Client communication:** No specific obligation

### Commercial photographer — Medium concern
Shoots products, uses Generative Expand to adapt aspect ratios for different
platforms. Client uses images for e-commerce and social advertising.
- **Disclosure:** Recommended to inform client about AI-assisted modifications
- **Machine-readable label:** Should be present (C2PA via Adobe tools)
- **Contract:** Include AI disclosure clause
- **Client responsibility:** Client should be aware of downstream obligations
  when publishing AI-modified content in advertising

### Photojournalist — High concern
Covers news events. Uses any AI editing beyond basic adjustments.
- **Disclosure:** Mandatory. Any generative modification must be declared
- **Metadata:** IPTC Digital Source Type must reflect AI usage
- **Editorial guidelines:** NPPA, Reuters, AP all require AI disclosure
- **Risk:** Loss of credibility, legal liability, platform removal

### Stock photographer — High concern
Sells on Adobe Stock, Shutterstock. Uses AI in workflow.
- **Platform policies:** Each platform has specific AI content policies
  (some allow, some restrict, some require separate labeling)
- **Copyright Directive:** Right to opt-out of AI training applies
- **Metadata:** Must accurately reflect creation method
- **Risk:** Incorrect labeling can lead to content removal and account suspension
