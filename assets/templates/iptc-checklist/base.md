# IPTC/C2PA Metadata Compliance Checklist

## Pre-Shoot Setup
- [ ] Create IPTC metadata template in your software with:
  - [ ] Creator: Your full name
  - [ ] Copyright Notice: © [Year] [Name]. All rights reserved.
  - [ ] Rights Usage Terms: Your default licensing terms
  - [ ] Credit Line: Your name / studio name
  - [ ] Contact Info: Email, website, phone
- [ ] Enable Content Credentials export in Lightroom/Photoshop preferences
- [ ] If camera supports C2PA (Leica M11-P, Nikon Z9/Z8/Zf, Sony A1/A9III): enable in camera settings

## On Import
- [ ] Apply IPTC metadata template to all imported images
- [ ] Verify Creator and Copyright fields are populated

## After Editing
- [ ] Determine Digital Source Type for each image:
  - `digitalCapture` — No AI generation used
  - `compositeWithTrainedAlgorithmicMedia` — Photo + AI-generated elements
  - `trainedAlgorithmicMedia` — Fully AI-generated
- [ ] Set Digital Source Type via:
  - Photoshop: File > File Info > IPTC Extension
  - ExifTool: `exiftool -DigitalSourceType="[value]" image.jpg`
  - Photo Mechanic: IPTC Stationary Pad

## On Export
- [ ] Verify all IPTC fields are populated
- [ ] Verify Content Credentials are attached (check in export settings)
- [ ] For stock/editorial: verify platform-specific required fields

## On Delivery
- [ ] Inform client that metadata is embedded
- [ ] Warn about platforms that strip metadata (Instagram, Facebook, X)
- [ ] For commercial clients: include metadata summary with delivery

## Verification
- [ ] Spot-check exported files with ExifTool: `exiftool -IPTC:all image.jpg`
- [ ] Verify Content Credentials at: https://contentcredentials.org/verify
