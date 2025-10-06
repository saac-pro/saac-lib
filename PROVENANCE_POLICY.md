# SAAC Provenance & Authorship Policy  
*Version 1.0 — Final for Signature (2025-10-06)*

**Project:** SAAC Pictogram Library (“Library”)  
**Copyright Holder:** SAAC sp. z o.o.  
**NIP:** 7123486771 **KRS:** 0001148143  
**Address:** Leona Frankowskiego 26, 20-736 Lublin, Poland  
**Legal Representative (President):** Katarzyna Smirnowa-Stankiewicz  
**Co-author / Technical Lead (optional):** Aliaksei Smironu  
**Jurisdiction:** Republic of Poland / European Union (eIDAS)

---

## 1. Purpose
This Policy establishes the origin, authorship and integrity controls for all pictograms and related materials comprising the SAAC Pictogram Library.  
It ensures legal certainty and traceability for public institutions, schools, non-profits and companies using the Library.

## 2. Definitions
- **Library** — collection of pictograms, metadata and packaging materials released by SAAC.  
- **Reference Set** — human-designed baseline icons and Style Guide defining visual DNA.  
- **AI-Assisted Output** — images generated with AI tools under human prompts, curation and approval.  
- **Release** — versioned package (ZIP) with icons, `manifest.json`, `LICENSE`, checksums and signatures.  
- **Contributors** — employees or contractors who create or review assets for SAAC.

## 3. Authorship & Ownership
1. All Reference Set assets are human-created by or for SAAC and constitute original works.  
2. AI-Assisted Output is produced under human creative direction (human-in-the-loop) and, once approved, is deemed authored and owned by **SAAC sp. z o.o.**  
3. SAAC also asserts rights as **database producer** (EU sui generis database right) over the Library and its metadata.  
4. The Library is distributed under **SAAC Custom License v1.0** (separate document). Use of the “SAAC” trademark is not licensed except for attribution.

## 4. Creation Process (Human → AI → Human)
1. **Reference Set & Style Guide:** SAAC designers create reference icons and define visual rules (stroke, grid, contrast, do/don’t).  
2. **AI Generation:** Each concept is prompted in the defined style; AI tools serve as instruments. Outputs are curated and normalized (e.g., SVGO).  
3. **Quality Assurance:** Icons undergo automated linting (viewBox, transparency, path limits) and manual review for clarity and cultural neutrality.  
4. **Approval:** Statuses Approved / Needs Fix / Reject; only Approved assets enter Releases.

## 5. Tooling & Third-Party Compliance
1. SAAC uses generative AI tools (including Google Vertex AI / ImageFX / Gemini) **strictly under their official Terms of Service**. Under these terms SAAC owns all rights to generated outputs.  
2. No third-party copyrighted materials are ingested or reused.  
3. Inbound licenses (CC BY, public domain, etc.) are recorded per asset in `manifest.json`. Copyleft licenses (GPL, CC BY-SA) are excluded from the core Library.  
4. All AI-assisted images are reviewed by human designers before release.

## 6. Contributors & Chain of Title (Polish law)
1. **Employees (utwór pracowniczy):** economic rights transfer to SAAC upon acceptance per employment contracts; contributors consent to SAAC exercising certain moral rights (modifications, publication without naming).  
2. **Contractors:** before contributing sign a rights-assignment covering fields of exploitation (pola eksploatacji): reproduction, distribution, public communication, adaptation, network use, and sublicensing under the SAAC License. Contractors waive objection to modifications to the extent permitted by law.  
3. Contributor agreements and acceptance logs are stored under `/legal/`.

## 7. Provenance Logging
For each icon (or batch) SAAC records: `concept_id, labels, pos, prompt, model, seed, created_at, reviewer_id, approval_status, svg_sha256, license_version, source_license`.  
Logs are immutable and time-stamped; icons can be reproduced from these records.

## 8. Release Integrity & Signatures
1. Each Release contains: `manifest.json`, `LICENSE`, `CHANGELOG.md`, icons, `SHA256SUMS.txt`, and a **qualified or Profil Zaufany electronic signature** over the checksum file plus qualified timestamp.  
2. Private keys are stored on secure devices (HSM/smart card); releases are archived ≥ 10 years under `/legal/releases/`.  
3. Profil Zaufany signatures are recognized as advanced electronic signatures under eIDAS and fully valid for Polish jurisdiction.

## 9. Privacy (RODO / GDPR)
SAAC processes reviewer identifiers under **legitimate interest** (Art. 6(1)(f) GDPR) for auditability.  
Processing complies with the **General Data Protection Regulation (EU 2016/679)** and the **Ustawa z dnia 10 maja 2018 r. o ochronie danych osobowych (Dz.U. 2018 poz. 1000)**.  
Data is minimized, access-controlled and retained only as long as needed for legal defense and integrity proofs. Data subjects may exercise their rights via the contact listed in the License.

## 10. Licensing & Attribution (Outbound)
1. Distributed under **SAAC Custom License v1.0**.  
2. Required attribution: “Pictogram source: SAAC Library (© SAAC sp. z o.o.), saac.example”.  
3. License defines usage rights and commercial fee tiers; no trademark license beyond attribution.  
4. Library provided *“as is”* without warranty.

## 11. Accessibility & Inclusivity
SAAC prioritizes clear, culturally neutral symbols for education and public use. Feedback channels are open for corrections and requests.

## 12. Governance & Amendments
1. Policy is versioned; amendments logged and digitally signed.  
2. In case of discrepancies between language versions, the **Polish** text prevails.  
3. Amendments do not retroactively affect previous releases unless explicitly stated.

## 13. Law & Forum
This Policy and related releases are governed by Polish law and applicable EU law.  
Disputes fall under the competent courts of **Lublin, Poland**.

---

**Digitally Signed (Profil Zaufany / qualified eIDAS):**  
**Katarzyna Smirnowa-Stankiewicz** — President, SAAC sp. z o.o.  
*(Optional)* **Aliaksei Smironu** — Co-author / Technical Lead
