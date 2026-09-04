<div align="center">

<img src="https://raw.githubusercontent.com/adi-Git-Hub/adi-Git-Hub/main/assets/header.svg" width="100%"/>

<br/>

⌁&nbsp;&nbsp;[<img src="https://img.shields.io/badge/GitHub-0d1117?style=flat-square&logo=github&logoColor=00F7FF" height="26"/>](https://github.com/adi-Git-Hub)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/LinkedIn-0d1117?style=flat-square&logo=linkedin&logoColor=00F7FF" height="26"/>](https://www.linkedin.com/in/aditya-dev-pande/)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/Portfolio-0d1117?style=flat-square&logo=vercel&logoColor=FF3CAC" height="26"/>](https://adi-git-hub.github.io/aditya-portfolio/)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/Email-0d1117?style=flat-square&logo=gmail&logoColor=FF3CAC" height="26"/>](mailto:aditya.dev.pande@gmail.com)

</div>

<br/>

## `01` ⌁ Identity

<div align="center">

<img src="https://raw.githubusercontent.com/adi-Git-Hub/adi-Git-Hub/main/assets/identity-terminal.svg" width="100%"/>

</div>

<br/>

## `02` ⌁ Engineering Focus

<table>
<tr>
<td width="50%" valign="top">

**FULL STACK ENGINEERING**
End-to-end product development, from UI to API to database

</td>
<td width="50%" valign="top">

**CLOUD ARCHITECTURE**
Designing systems around managed cloud infrastructure

</td>
</tr>
<tr>
<td width="50%" valign="top">

**DEVOPS & CI/CD**
Automated build → test → deploy workflows

</td>
<td width="50%" valign="top">

**SYSTEM DESIGN**
Structuring services, data and APIs before writing code

</td>
</tr>
<tr>
<td width="50%" valign="top">

**DEVSECOPS**
Treating auth, secrets and access control as first-class concerns

</td>
<td width="50%" valign="top">

**INFRASTRUCTURE AS CODE**
Versioned, reviewable infrastructure and schema changes

</td>
</tr>
<tr>
<td width="50%" valign="top">

**PERFORMANCE**
Identifying and fixing real bottlenecks, not guessing at them

</td>
<td width="50%" valign="top">

</td>
</tr>
</table>

<br/>

## `03` ⌁ Tech Stack

<table>
<tr><td><b>Frontend</b></td><td>

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

</td></tr>
<tr><td><b>Backend</b></td><td>

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

</td></tr>
<tr><td><b>Databases</b></td><td>

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

</td></tr>
<tr><td><b>Cloud</b></td><td>

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)

</td></tr>
<tr><td><b>DevOps & CI/CD</b></td><td>

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)

</td></tr>
<tr><td><b>Infrastructure</b></td><td>

![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)

</td></tr>
<tr><td><b>Tools & Platform</b></td><td>

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

</td></tr>
</table>

<br/>

## `04` ⌁ Engineering & Architecture

The diagram below is the request-flow model I default to when designing a new system — **a set of principles, not a claim that this exact stack is deployed in a specific production system.** Project-specific architecture is documented under Featured Projects.

```
┌──────────────────────────┐
│          CLIENT          │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│    FRONTEND (React /     │
│         Next.js)         │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│            API           │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│     BACKEND SERVICES     │
│    (Node.js / Python)    │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│     DATABASE / CACHE     │
│   (PostgreSQL / Redis)   │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│   CLOUD INFRASTRUCTURE   │
└─────────────┬────────────┘
              │
┌─────────────▼────────────┐
│   CI/CD + OBSERVABILITY  │
└──────────────────────────┘
```

How I think about each concern, grounded in the projects below where I can point to it:

| Concern | Approach |
|---|---|
| **Scalability** | Split systems into bounded pieces — auth, bookings and payments as separate route/controller layers — so one part changes without reshaping the rest *(see CloudCar)* |
| **Reliability** | Don't trust a single channel for critical state — live order tracking runs over WebSockets with a polling fallback, since realtime alone isn't reliable on shared Wi-Fi *(see Jainism Cake & Café)* |
| **Caching** | Cache read-heavy, slow-changing data close to where it's used, and invalidate it deliberately rather than on a blind timer |
| **APIs & Contracts** | One shared source of truth for pricing/data shape between client and server, so the client can never send something the server didn't expect *(see Jainism Cake & Café)* |
| **Databases** | Schema changes as versioned, numbered migrations, not manual edits *(see CloudCar)* |
| **Authentication** | Hashed credentials and JWTs, with role checks enforced on the server — a 403, not just a hidden button *(see both projects)* |
| **CI/CD** | Automated build → deploy on push via GitHub Actions |
| **Infrastructure** | Config through environment variables; deployment checklists and hardening notes committed alongside the code, not kept in someone's head |
| **Monitoring / Observability** | Principle: surface failure states explicitly instead of failing silently — an area I'm actively deepening with formal tooling |
| **Security** | Password hashing, signature-verified webhooks, and authorization checks that run server-side |

<br/>

## `05` ⌁ DevOps Pipeline

<div align="center">

`CODE` → `GIT` → `CI` → `TESTS` → `DOCKER` → `IaC` → `CLOUD DEPLOYMENT` → `MONITORING` → `ALERTS`

</div>

| Stage | Why it exists |
|---|---|
| **Code** | Every change is scoped and reviewable before it merges |
| **Git** | Branching and history give a safe way to collaborate and roll back |
| **CI** | Catch integration issues before they reach anyone else |
| **Automated Tests** | Verify behavior automatically instead of by hand, every time |
| **Docker** | The same artifact runs the same way in dev, staging and production |
| **Infrastructure as Code** | Infra changes are reviewed and reproducible, not manual clicks in a console |
| **Cloud Deployment** | Ship a verified artifact without manual server access |
| **Monitoring** | Know a system is unhealthy before a user has to report it |
| **Alerts** | Get notified early enough that a small issue doesn't become an outage |

<br/>

## `06` ⌁ Featured Projects

<table>
<tr><td width="100%">

### CloudCar — Cloud-Native Car Rental Platform

*Browse cars, book a vehicle and receive a secure email confirmation — a full-stack rental flow from UI to database.*

**Architecture**
`React (Vite) client → Express REST API → PostgreSQL` — schema versioned through numbered SQL migrations

**Engineering**
- JWT authentication with bcrypt-hashed passwords
- Auth and bookings implemented as separate route/controller layers
- File uploads handled via Multer; booking confirmations sent via Nodemailer
- 4 numbered migrations (`001`–`004`) instead of ad-hoc schema edits
- Deployment checklist and database-hardening notes committed with the code

**Stack**
React · Vite · Tailwind CSS · React Three Fiber · Node.js · Express · PostgreSQL · JWT

**Links**
[Repository](https://github.com/adi-Git-Hub/Cloud-Native-Full-stack-DevOps-Intregated-E-Car_Website) &nbsp;·&nbsp; [Live Demo](https://3d-e-commarce-new-update.vercel.app)

</td></tr>
</table>

<br/>

<table>
<tr><td width="100%">

### Jainism Cake & Café — Smart Ordering Platform

*A customer scans a table QR code, orders, pays and tracks the kitchen live — no app, login or OTP.*

**Architecture**
`React client ↔ Socket.IO / REST ↔ Express API ↔ SQLite` — shared TypeScript contracts between client and server

**Engineering**
- One shared pricing module prices every order server-side, so a client can never be charged something it wasn't shown
- Real-time order tracking over Socket.IO rooms with a polling fallback for unreliable Wi-Fi
- Role-based staff portal (Admin / Counter / Kitchen) enforced both in the UI and on the server, not just hidden buttons
- Pluggable payment provider interface — mock by default; a Razorpay adapter is implemented with HMAC signature verification, documented as untested against live credentials
- Money stored as integer rupees to avoid floating-point errors; every row scoped by a `tenant_id`

**Stack**
React 19 · TypeScript · Vite · Tailwind CSS · Express · Socket.IO · SQLite

**Links**
[Repository](https://github.com/adi-Git-Hub/QR-Menu-System-jainism-cake-cafe) &nbsp;·&nbsp; Live Demo — _not publicly deployed_

</td></tr>
</table>

<br/>

## `07` ⌁ GitHub Analytics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=adi-Git-Hub&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=00F7FF&icon_color=FF6EC7&text_color=c9d1d9" width="44%"/>
<img src="https://streak-stats.demolab.com?user=adi-Git-Hub&theme=tokyonight&hide_border=true&background=0d1117&ring=00F7FF&fire=FF6EC7&currStreakLabel=00F7FF" width="44%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=adi-Git-Hub&theme=react-dark&bg_color=0d1117&color=00F7FF&line=FF6EC7&point=ffffff&hide_border=true" width="80%"/>

</div>

<br/>

## `08` ⌁ Currently Building

Currently building:
→ `<update this>`
→ `<update this>`
→ `<update this>`

<br/>

## `09` ⌁ Engineering Principles

- Automation over repetition
- Security by design
- Observability over assumptions
- Measurable performance
- Infrastructure as Code
- Clean architecture
- Reliability over shortcuts

<br/>

<div align="center">

<img src="https://raw.githubusercontent.com/adi-Git-Hub/adi-Git-Hub/main/assets/footer-banner.svg" width="100%"/>

⌁&nbsp;&nbsp;[<img src="https://img.shields.io/badge/GitHub-0d1117?style=flat-square&logo=github&logoColor=00F7FF" height="26"/>](https://github.com/adi-Git-Hub)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/LinkedIn-0d1117?style=flat-square&logo=linkedin&logoColor=00F7FF" height="26"/>](https://www.linkedin.com/in/aditya-dev-pande/)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/Portfolio-0d1117?style=flat-square&logo=vercel&logoColor=FF3CAC" height="26"/>](https://adi-git-hub.github.io/aditya-portfolio/)&nbsp;&nbsp;|&nbsp;&nbsp;[<img src="https://img.shields.io/badge/Email-0d1117?style=flat-square&logo=gmail&logoColor=FF3CAC" height="26"/>](mailto:aditya.dev.pande@gmail.com)

</div>
