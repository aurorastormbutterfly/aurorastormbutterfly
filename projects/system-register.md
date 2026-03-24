# Case Study: UK Home Office System Register

### Context
During my tenure at **Thoughtworks**, I contributed to the development of the **System Register**, an open-source platform designed for the **UK Home Office**. The system’s purpose is to crowdsource and manage a comprehensive record of organisational systems and their associated risks, providing a clear audit trail for decision-makers.

### Technical Solution
The project required a high-integrity, scalable architecture capable of handling complex data relationships while meeting strict government security and accessibility standards.

* **Backend**: Java 11 with **Quarkus** (Supersonic Subatomic Java), leveraging its low footprint for cloud-native deployment.
* **Frontend**: **React** SPA focused on high performance and data density.
* **Data Visualization**: **D3.js** for custom, interactive risk heatmaps and system relationship graphs.
* **Architecture**: **Event Sourcing** to ensure a 100% immutable audit log of all system changes.
* **Database**: PostgreSQL (Managed).
* **Compliance**: Strictly adhered to **GDS (Government Digital Service)** standards and **WCAG 2.1** accessibility requirements.

---

### Key Architectural Pillar: Event Sourcing
Unlike traditional CRUD systems, the System Register uses an **Event Sourcing** pattern. Every change to a system record is stored as a discrete event in an immutable log. 



This was critical for a government-level risk tool because:
1. **Auditability**: We can replay the history of any system to see exactly what its risk profile looked like at any point in time.
2. **Consistency**: It allows the backend to decouple the Write model (recording the risk) from the Read model (visualising the data in D3.js).

---

### Data Visualisation with D3.js
A core requirement was making abstract risk data tangible. I utilised **D3.js** within the React ecosystem to build custom visualisations that:
* Mapped hierarchical system dependencies.
* Provided interactive Risk Matrix views.
* Maintained **SVG accessibility**, ensuring that screen reader users could navigate the visual data through hidden ARIA-compliant tables and descriptions.

---

### Quality & Security Engineering
As the project was destined for a high-security environment, we built in a number of robust and security checks, including:
* **Secret Detection**: Integrated `detect-secrets` via `pre-commit` hooks to prevent any credentials from entering the version control system.
* **Automated Testing**: Utilised a robust testing pyramid including Unit tests (JUnit), Integration tests (Quarkus Test), and E2E suites.
* **GDS Compliance**: Conducted regular accessibility audits to ensure the platform was inclusive by design.

---

### Key Outcomes
* Delivered a production-ready, open-source tool currently available for public sector adaptation.
* Successfully balanced complex architectural patterns (Event Sourcing) with a user-friendly, GDS-compliant frontend.
* Established a "Security-First" developer workflow that became a standard for the project's contributors.