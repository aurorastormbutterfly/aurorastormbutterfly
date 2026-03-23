# Case Study: Gamified Life Coaching & Dynamic Course Portal

### Context
The project involved building a high-performance, subscription-based learning platform. The goal was to deliver a personalised experience where course recommendations and "gamified" goals were dynamically generated based on user quiz results and focus areas.

### Technical Solution
I architected a decoupled full-stack application hosted on **Google Cloud Platform (GCP)**. The system uses **Next.js** for a high-performance frontend and a **Node.js/Express** backend to manage complex business logic, gamification engines, and secure data persistence.

* **Frontend**: Next.js (SSG for public site, SSR for member portals).
* **Backend**: Node.js & Express (RESTful API).
* **CMS**: Payload CMS (Headless) for content authoring and course management.
* **Database**: Managed PostgreSQL on GCP (Cloud SQL).
* **Infrastructure**: GCP (App Engine/Cloud Run), Cloud Storage for media.
* **Integrations**: Stripe (Billing), Auth0 or Firebase (Identity).

---

### System Architecture (C4 Model - Level 2)

![level 2 diagram showing interaction between system components and external users](../projects/assets/lcp-architecture.png)