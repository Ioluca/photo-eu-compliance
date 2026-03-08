# C2PA & IPTC Metadata — Reference Guide for Photographers

## Last updated: 2025-08-02

---

## Table of Contents
1. Why Metadata Matters for Compliance
2. IPTC Photo Metadata — Essential Fields
3. IPTC Digital Source Type (2024 Vocabulary)
4. C2PA Content Credentials
5. Software-Specific Setup
6. Workflow Integration

---

## 1. Why Metadata Matters

Metadata serves three compliance functions:

1. **Proof of authorship:** IPTC copyright fields establish you as the creator
2. **AI transparency:** IPTC Digital Source Type declares how the image was made
3. **Provenance chain:** C2PA Content Credentials provide cryptographic proof
   of the image's origin and every modification made to it

Under the AI Act Art. 50, AI-generated content must be marked in a
**machine-readable format**. Metadata is how this is done in practice.

---

## 2. IPTC Photo Metadata — Essential Fields

The IPTC standard (maintained by iptc.org) defines metadata fields
embedded in image files. These are the fields every photographer
should fill on every image:

### Always fill

| IPTC Field | What to enter | Why |
|-----------|---------------|-----|
| **Creator** | Your full name | Authorship attribution |
| **Copyright Notice** | © [Year] [Your Name]. All rights reserved. | Legal copyright notice |
| **Rights Usage Terms** | Your licensing terms (e.g., "All rights reserved" or specific license) | Defines permitted use |
| **Credit Line** | Your name or studio name | For publication credit |
| **Source** | Your studio/agency name | Origin of the image |

### Fill when relevant

| IPTC Field | When | What to enter |
|-----------|------|---------------|
| **Description** | Always recommended | What the image shows |
| **Keywords** | For stock/searchability | Descriptive keywords |
| **Location** | When location matters | City, state, country |
| **Date Created** | Always | Date of capture |
| **Instructions** | For editorial | Usage restrictions or notes |

---

## 3. IPTC Digital Source Type (2024 Update)

In 2024, IPTC updated the Digital Source Type vocabulary to address AI.
This field declares HOW the image was created.

### Vocabulary values relevant to photographers

| Value | Code | When to use |
|-------|------|-------------|
| **Digital capture** | `digitalCapture` | Straight from camera, no AI generation |
| **Digitized from negative** | `negativeFilm` | Scanned film |
| **Algorithmically enhanced** | `algorithmicallyEnhanced` | AI processing only (Denoise, AI masks, auto-adjust). No new content generated |
| **Composite with trained algorithmic media** | `compositeWithTrainedAlgorithmicMedia` | Photo combined with AI-generated elements (AI sky, generative expand, AI background) |
| **Trained algorithmic media** | `trainedAlgorithmicMedia` | Fully AI-generated image (Midjourney, DALL-E, Firefly Image Generator) |
| **Composite** | `composite` | Traditional compositing without AI |

### Decision guide

```
Did you take this photo with a camera?
  → Yes → Did you apply AI generation of any kind?
            → No (or only Denoise/masks/auto) → digitalCapture
               (algorithmicallyEnhanced is acceptable but optional)
            → Yes, minor AI fill (small object removal) →
               compositeWithTrainedAlgorithmicMedia
            → Yes, significant AI (expand, sky replace, AI elements) →
               compositeWithTrainedAlgorithmicMedia
  → No → Was it fully AI-generated?
            → Yes → trainedAlgorithmicMedia
            → No (traditional composite) → composite
```

### How to set in software

**Lightroom Classic:**
- Not natively exposed in the UI
- Use File > File Info > IPTC Extension > Digital Source Type
- Or set via ExifTool after export:
  ```bash
  exiftool -DigitalSourceType="digitalCapture" image.jpg
  ```

**Photoshop:**
- File > File Info > IPTC Extension tab
- Digital Source Type dropdown

**Photo Mechanic:**
- IPTC Stationary Pad > Digital Source Type field

**ExifTool (command line):**
```bash
# For a camera capture
exiftool -DigitalSourceType="http://cv.iptc.org/newscodes/digitalsourcetype/digitalCapture" image.jpg

# For AI-composite
exiftool -DigitalSourceType="http://cv.iptc.org/newscodes/digitalsourcetype/compositeWithTrainedAlgorithmicMedia" image.jpg

# For fully AI-generated
exiftool -DigitalSourceType="http://cv.iptc.org/newscodes/digitalsourcetype/trainedAlgorithmicMedia" image.jpg
```

IPTC reference: https://cv.iptc.org/newscodes/digitalsourcetype/

---

## 4. C2PA Content Credentials

### What they are

C2PA (Coalition for Content Provenance and Authenticity) is an open standard
that attaches a cryptographic provenance record to media files. It records:

- **Origin:** What device captured the image (camera model, software)
- **Edits:** What modifications were made and with which tools
- **AI usage:** Whether AI generation was involved
- **Identity:** Who claims authorship (optional, can be anonymous)

Think of it as a tamper-evident seal showing the complete history of an image.

### Who supports it

- **Adobe:** Full support in Photoshop, Lightroom, Firefly (enabled by default)
- **Leica:** M11-P and later cameras embed C2PA at capture
- **Nikon:** Z9, Z8, Zf with firmware updates
- **Sony:** Alpha 1, Alpha 9 III with firmware updates
- **Canon:** Announced support, timeline pending
- **Microsoft:** Bing Image Creator embeds C2PA
- **Google:** Implementing in some products

### How to enable

**Lightroom / Photoshop:**
1. Go to Edit > Preferences > Content Credentials (Lightroom: Settings)
2. Toggle "Attach Content Credentials to exported files"
3. Optionally sign in with your Adobe account for identity verification
4. Content Credentials will be embedded on export

**Camera-level (Leica, Nikon, Sony):**
- Enable in camera settings
- C2PA data is embedded at the moment of capture
- Maintained through the editing pipeline if using compatible software

### Verification

Anyone can verify Content Credentials at:
https://contentcredentials.org/verify

Upload or drag an image to see its full provenance history.

### Limitations

- **Not all platforms preserve C2PA:** Social media uploads often strip metadata.
  Instagram, Facebook, Twitter/X currently strip most metadata including C2PA.
- **Adoption is still growing:** Not all cameras or software support it yet
- **Not legally mandated yet:** AI Act requires machine-readable marking but
  does not specifically mandate C2PA (though it is the most established standard)
- **Can be removed:** Like all metadata, C2PA can be stripped. It is not DRM.

---

## 5. Workflow Integration

### Pre-shoot setup
1. Create an IPTC metadata template in Lightroom with your defaults:
   - Creator, Copyright Notice, Rights Usage Terms, Contact Info
2. Enable Content Credentials in export preferences
3. If your camera supports C2PA, enable it

### During import
- Apply your IPTC template on import
- This ensures every image starts with your copyright information

### During editing
- If you use AI tools, note which ones for later metadata setting
- Adobe tools automatically log AI usage in Content Credentials

### On export
1. Verify IPTC fields are populated
2. Set Digital Source Type according to the decision guide above
3. Ensure Content Credentials are attached
4. For stock/editorial: double-check all fields match platform requirements

### Delivery to clients
- Inform clients that metadata is embedded and should be preserved
- Warn that some platforms strip metadata on upload
- For commercial clients: provide a metadata summary document
  alongside the images
