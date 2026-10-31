# Technical Quality-Control & Verification Report (Final QC Pass)

**Repository:** [`tanmay9783/tanmay9783`](https://github.com/tanmay9783/tanmay9783)  
**Candidate:** Tanmay Agrawal  
**Audit Scope:** Quality-Control Pass — Absolute Claims Elimination, Evidential Alignment, Asset Validation  
**Date of Audit:** October 2026  

---

## 1. Files Changed & Asset Status

| File | Status | Nature of Changes |
| :--- | :--- | :--- |
| **`README.md`** | **Updated & Verified** | Replaced "Production & Implementation Stack" with "Technologies Used in Projects"; updated Rootless Podman claims to risk-reduction framing; updated RabbitMQ durability descriptions; changed DropX to temporary file sharing; changed Sanjeevni to AI-Assisted Patient Intake; updated hackathon and certifications with verified Credly and Certmetrics links. |
| **`TECHNICAL_VERIFICATION_REPORT.md`** | **Updated & Verified** | Updated with final QC audit log, technical claims verification, and asset resolution checks. |
| **`ASSET_SETUP_GUIDE.md`** | **Verified** | Up to date with all external SVG services and GitHub Actions configuration. |
| **`assets/projects/`** | **Verified (Committed)** | All project preview assets (`coditorium-logo.png`, `dropx-preview.png`, `nijisamvad-preview.png`, `planrova-preview.png`, `sanjeevni-preview.png`) verified committed and resolving HTTP 200 on `main`. |

---

## 2. Broken Assets & Image Resolution Audit

All local and remote assets referenced in `README.md` were tested and verified:

```
[Local Asset Audit - assets/projects/]
✓ assets/projects/coditorium-logo.png   (499,082 bytes) -> Resolves 200 on main
✓ assets/projects/dropx-preview.png     (487,997 bytes) -> Resolves 200 on main
✓ assets/projects/nijisamvad-preview.png (75,150 bytes) -> Resolves 200 on main
✓ assets/projects/planrova-preview.png  (148,150 bytes) -> Resolves 200 on main
✓ assets/projects/sanjeevni-preview.png (763,900 bytes) -> Resolves 200 on main

[External Badge & Card Endpoints]
✓ Typing SVG (readme-typing-svg.demolab.com)            -> HTTP 200 OK
✓ SkillIcons Vector Grid (skillicons.dev)               -> HTTP 200 OK
✓ GitHub Streak Stats (streak-stats.demolab.com)        -> HTTP 200 OK
✓ GitHub Stats Card (github-readme-stats-eight-theta)   -> HTTP 200 OK
✓ Top Languages Card (github-readme-stats-eight-theta)  -> HTTP 200 OK
✓ LeetCode Stats Card (leetcard.jacoblin.cool)          -> HTTP 200 OK
✓ Codeforces Card (codeforces-readme-stats)             -> HTTP 200 OK
✓ Shields.io Action Buttons                             -> HTTP 200 OK
```

---

## 3. Technical Claims Corrected (Final QC Pass)

1. **Stack Categorization:** Replaced "Production & Implementation Stack" with **"Technologies Used in Projects"**, maintaining a clean separation from technologies being explored.
2. **NijiSamvad Cryptographic Precision:** Changed heading to **"Client-Side Encrypted Communication & WebRTC Mesh"**. Removed all remaining "Zero-Knowledge" references in favor of client-side AES-256-GCM symmetric encryption with an ephemeral blind-relay server.
3. **Rootless Podman Security Framing:** Replaced absolute claims of "eliminating root privilege escalation vectors" with risk-reduction framing: **"substantially reduce the host attack surface by executing untrusted containers without root privileges, mitigating root privilege escalation vectors on the host system."**
4. **RabbitMQ Durability Accuracy:** Replaced "guarantee durable delivery" with precise implementation details verified in `apps/backend/src/modules/submissions/queue.service.ts`: durable queue assertions (`{ durable: true }`), disk-persisted delivery (`{ persistent: true }`), and explicit manual worker acknowledgments (`{ noAck: false }`).
5. **DropX Terminology:** Replaced "high-speed streaming" and "ephemeral data utility" with **"temporary cross-device file sharing platform"**.
6. **Sanjeevni AI Scoping:** Replaced "Autonomous" descriptions with **"AI-Assisted Patient Intake"**, explicitly documenting that while form responses log locally to SQLite, multimodal AI extraction requires connectivity to reach LLM endpoints.
7. **Certifications & Hackathon Credential Verification:** Verified against official issuing bodies:
   - *AWS Certified Cloud Practitioner* (Amazon Web Services — [Verify Credential](https://cp.certmetrics.com/amazon/en/public/verify/credential/fac9701f985443a3a5cad85982cc6520))
   - *AWS Certified AI Practitioner* (Amazon Web Services — [Verify Credential](https://cp.certmetrics.com/amazon/en/public/verify/credential/4ad652a9eeee41e39af0dfabae4fcc8a))
   - *AWS Academy Graduate — Generative AI Foundations* (AWS Academy — [Verify Credly Badge](https://www.credly.com/earner/earned/badge/ff32dd8b-470b-4dd4-b7da-536382d97959))
   - *NIT Jalandhar Hackathon — Top 10 Finalist* (Ranked in Top 10 out of 100+ teams in a 36-hour sprint).

---

## 4. Mermaid Architecture Rendering Status

- **Diagram 1 (Coditorium Judge Execution Pipeline):** Validated `flowchart TD`. Cylinder node labels formatted cleanly with no conflicting nested parentheses.
- **Diagram 2 (NijiSamvad Cryptographic Key Derivation & Ephemeral Signaling):** Validated `sequenceDiagram`. Autonumbering, participant mappings, and note boxes verified for native GitHub rendering.

---

## 5. Remaining Technical Limitations (Documented in Profile)

- **Coditorium:** Per-submission container initialization incurs container cold-start latency compared to long-running worker processes; warm container pooling and microVM virtualization are future milestones.
- **NijiSamvad:** Relies on a pre-shared room passphrase without an asymmetric Double Ratchet protocol (Signal Protocol); does not provide Perfect Forward Secrecy (PFS).
- **DropX:** In-memory `express.raw()` upload buffering caps single-file uploads at 100MB rather than using backpressure-controlled streaming pipes.
- **Planrova:** Android alarms rely on `SCHEDULE_EXACT_ALARM` permissions and remain subject to OEM battery optimization overrides.
- **Sanjeevni AI:** Speech recognition accuracy depends on clinic ambient acoustic noise; designed as a triage assistant rather than an autonomous diagnostic device.
- **Terraform Multi-Env:** Deploys compute into default VPC subnets rather than a custom multi-tier VPC topology.

---

## 6. Repository Metadata Recommendation (Manual Setup via GitHub UI)

Since GitHub SSH keys do not authenticate GitHub REST API calls, configure these values via the **About** section on [github.com/tanmay9783/tanmay9783](https://github.com/tanmay9783/tanmay9783):

- **Description:** `Full-Stack Developer & Software Engineer | Backend Systems, Distributed Architecture & Cloud Infrastructure`
- **Website:** `https://github.com/tanmay9783/portfolio`
- **Topics:** `full-stack`, `backend`, `distributed-systems`, `system-design`, `nestjs`, `rabbitmq`, `podman`, `webrtc`, `cryptography`, `terraform`, `aws`
