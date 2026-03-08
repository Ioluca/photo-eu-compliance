# 📷 photo-eu-compliance

**EU regulatory compliance toolkit for professional photographers.**

A Claude skill that generates personalized compliance packages covering AI Act, GDPR, and Copyright Directive — tailored to your photography workflow.

🇬🇧 [English](#english) | 🇮🇹 [Italiano](#italiano) | 🇩🇪 [Deutsch](#deutsch) | 🇫🇷 [Français](#français) | 🇪🇸 [Español](#español)

---

## English

### What it does

You answer 8 questions about your photography workflow. The skill generates **7 personalized files** ready to use:

| # | Output | Format |
|---|--------|--------|
| 1 | Compliance Checklist | PDF |
| 2 | AI Disclosure Decision Tree | HTML |
| 3 | Model Release (GDPR-compliant) | DOCX |
| 4 | AI Training Opt-Out Letter | DOCX |
| 5 | IPTC/C2PA Metadata Guide | PDF |
| 6 | AI Disclosure Contract Clause | DOCX |
| 7 | Regulatory Changelog | MD |

Every document includes specific legal references (article numbers + EUR-Lex links) and is calibrated to your genre, country, and AI tools.

### The key principle

**Processing pixels ≠ Generating pixels.**

AI Denoise, masks, auto-adjust → No disclosure needed.
Generative Remove, Expand, AI sky replacement → Disclosure may be required.

This skill helps you understand where the line is for your specific case.

### Regulations covered

- **AI Act** (Reg. EU 2024/1689) — Art. 50 transparency, Art. 53-55 GPAI
- **GDPR** (Reg. EU 2016/679) — Consent, right to image, Art. 85 derogation
- **Copyright Directive** (Dir. EU 2019/790) — Art. 4 opt-out, Art. 15, Art. 17
- **GPAI Code of Practice** (July 2025) — Copyright chapter
- **C2PA / IPTC standards** — Content Credentials, Digital Source Type
- **National laws:** Italy, Germany, France, Spain (more welcome via PR)

### Installation

**Claude.ai:**
1. Download the [latest release](https://github.com/Ioluca/photo-eu-compliance/releases) (.zip)
2. Go to Settings > Capabilities > Skills
3. Click "Upload skill" and select the zip
4. Done — the skill activates automatically when relevant

**Claude Code:**
Copy the skill folder to your skills directory.

### Usage

Just ask Claude something like:

> "I'm a wedding photographer in Milan. I use Generative Remove in Lightroom. Do I need to worry about the AI Act?"

The skill will guide you through the interview and generate your package.

### Contributing

This is an open-source project. Contributions are welcome:

- **Add a country:** Create `references/national/[country].md` and submit a PR
- **Add a language:** Create clause templates in `assets/templates/*/[lang].md`
- **Fix or update legal references:** Regulations change — help keep them current
- **Report issues:** Open an issue if you find incorrect information

### Disclaimer

⚠️ This skill provides informational guidance, not legal advice. Regulatory interpretation varies by jurisdiction and evolves over time. Consult a qualified legal professional for binding guidance on your specific situation.

### Author

Created by [Luca Cazzaniga](https://substack.com/@lucacazzaniga) — photographer, AI practitioner, and author of [Il Tecnologo](https://iltecnologo.substack.com) on Substack.

### License

MIT — see [LICENSE](LICENSE)

---

## Italiano

### Cosa fa

Rispondi a 8 domande sul tuo workflow fotografico. La skill genera **7 file personalizzati** pronti all'uso:

| # | Output | Formato |
|---|--------|---------|
| 1 | Checklist di Compliance | PDF |
| 2 | Decision Tree Disclosure AI | HTML |
| 3 | Model Release (conforme GDPR) | DOCX |
| 4 | Lettera Opt-Out Training AI | DOCX |
| 5 | Guida Metadati IPTC/C2PA | PDF |
| 6 | Clausola Contrattuale Disclosure AI | DOCX |
| 7 | Changelog Normativo | MD |

Ogni documento include riferimenti legali specifici (articoli + link EUR-Lex) ed è calibrato sul tuo genere fotografico, paese e strumenti AI.

### Il principio chiave

**Processare pixel ≠ Generare pixel.**

AI Denoise, maschere, regolazioni automatiche → Nessun obbligo di disclosure.
Generative Remove, Expand, sostituzione cielo AI → La disclosure potrebbe essere necessaria.

Questa skill ti aiuta a capire dov'è il confine per il tuo caso specifico.

### Normative coperte

- **AI Act** (Reg. UE 2024/1689) — Art. 50 trasparenza, Art. 53-55 GPAI
- **GDPR** (Reg. UE 2016/679) — Consenso, diritto all'immagine, deroga Art. 85
- **Direttiva Copyright** (Dir. UE 2019/790) — Art. 4 opt-out, Art. 15, Art. 17
- **Codice di Condotta GPAI** (luglio 2025) — Capitolo copyright
- **Standard C2PA / IPTC** — Content Credentials, Digital Source Type
- **Leggi nazionali:** Italia, Germania, Francia, Spagna (altre benvenute via PR)

### Installazione

**Claude.ai:**
1. Scarica l'[ultima release](https://github.com/Ioluca/photo-eu-compliance/releases) (.zip)
2. Vai in Settings > Capabilities > Skills
3. Clicca "Upload skill" e seleziona lo zip
4. Fatto — la skill si attiva automaticamente quando serve

### Uso

Scrivi a Claude qualcosa tipo:

> "Sono un fotografo di matrimoni a Milano. Uso il Generative Remove di Lightroom. Devo preoccuparmi per l'AI Act?"

La skill ti guida nell'intervista e genera il tuo pacchetto.

### Contribuire

Questo è un progetto open source. Contributi benvenuti:

- **Aggiungi un paese:** Crea `references/national/[paese].md` e apri una PR
- **Aggiungi una lingua:** Crea i template delle clausole in `assets/templates/*/[lingua].md`
- **Correggi o aggiorna i riferimenti legali:** Le normative cambiano — aiuta a tenerle aggiornate

### Disclaimer

⚠️ Questa skill fornisce una guida informativa, non consulenza legale. L'interpretazione normativa varia per giurisdizione e si evolve nel tempo. Consulta un professionista qualificato per indicazioni vincolanti sulla tua situazione specifica.

### Autore

Creata da [Luca Cazzaniga](https://substack.com/@lucacazzaniga) — fotografo, AI practitioner e autore di [Il Tecnologo](https://iltecnologo.substack.com) su Substack.

---

## Deutsch

### Was es macht

Beantworte 8 Fragen zu deinem Fotografie-Workflow. Die Skill generiert **7 personalisierte Dateien**, sofort einsatzbereit: Compliance-Checkliste (PDF), KI-Disclosure Decision Tree (HTML), Model Release DSGVO-konform (DOCX), Opt-Out-Brief KI-Training (DOCX), IPTC/C2PA-Metadaten-Leitfaden (PDF), KI-Disclosure-Vertragsklausel (DOCX), regulatorisches Changelog (MD).

### Das Schlüsselprinzip

**Pixel verarbeiten ≠ Pixel erzeugen.**

KI-Rauschreduzierung, Masken, automatische Anpassungen → Keine Offenlegungspflicht.
Generative Remove, Expand, KI-Himmelersetzung → Offenlegung kann erforderlich sein.

### Installation

1. Lade das [neueste Release](https://github.com/Ioluca/photo-eu-compliance/releases) herunter (.zip)
2. Gehe zu Settings > Capabilities > Skills in Claude.ai
3. Klicke "Upload skill" und wähle die ZIP-Datei

### Beitragen

Erstelle `references/national/[land].md` für dein Land und öffne einen Pull Request.

---

## Français

### Ce que ça fait

Répondez à 8 questions sur votre flux de travail photographique. La skill génère **7 fichiers personnalisés** prêts à l'emploi : checklist de conformité (PDF), arbre de décision divulgation IA (HTML), autorisation de droit à l'image conforme RGPD (DOCX), lettre d'opt-out entraînement IA (DOCX), guide métadonnées IPTC/C2PA (PDF), clause contractuelle divulgation IA (DOCX), changelog réglementaire (MD).

### Le principe clé

**Traiter des pixels ≠ Générer des pixels.**

Débruitage IA, masques, ajustements automatiques → Aucune obligation de divulgation.
Suppression générative, expansion, remplacement de ciel IA → La divulgation peut être requise.

### Installation

1. Téléchargez la [dernière version](https://github.com/Ioluca/photo-eu-compliance/releases) (.zip)
2. Allez dans Settings > Capabilities > Skills dans Claude.ai
3. Cliquez "Upload skill" et sélectionnez le zip

### Contribuer

Créez `references/national/[pays].md` pour votre pays et ouvrez une Pull Request.

---

## Español

### Qué hace

Responde 8 preguntas sobre tu flujo de trabajo fotográfico. La skill genera **7 archivos personalizados** listos para usar: checklist de cumplimiento (PDF), árbol de decisión divulgación IA (HTML), autorización de imagen conforme RGPD (DOCX), carta de opt-out entrenamiento IA (DOCX), guía de metadatos IPTC/C2PA (PDF), cláusula contractual divulgación IA (DOCX), changelog regulatorio (MD).

### El principio clave

**Procesar píxeles ≠ Generar píxeles.**

Reducción de ruido IA, máscaras, ajustes automáticos → Sin obligación de divulgación.
Eliminación generativa, expansión, reemplazo de cielo IA → La divulgación puede ser necesaria.

### Instalación

1. Descarga la [última versión](https://github.com/Ioluca/photo-eu-compliance/releases) (.zip)
2. Ve a Settings > Capabilities > Skills en Claude.ai
3. Haz clic en "Upload skill" y selecciona el zip

### Contribuir

Crea `references/national/[pais].md` para tu país y abre un Pull Request.

---

## Regulatory Baseline

This skill's legal references are current as of **August 2, 2025** (GPAI Code of Practice entry into force). The skill can check for updates on demand via web search.

## What's Next

- [ ] Additional country modules (Netherlands, Belgium, Portugal, Austria, Poland)
- [ ] German, French, Spanish GDPR clause templates
- [ ] Opt-out letter localized variants
- [ ] Integration with Claude Code workflows
- [ ] Community-contributed case law references
