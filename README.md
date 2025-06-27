# RealBuild - Realistic PC system analysis on a new level

**An open source vision project for everyone who wants to *really* understand their system.

---

## Idea & motivation

Many PC configurators only show: “That fits.”  
Some simulate builds visually.  
But **none of these tools think for themselves - realistically, data-based, dynamically**.

**RealBuild** is designed to do just that:
- Realistically calculate PSU utilization (incl. OC, peripherals, pumps, RGB)
- Detect thermal bottlenecks (airflow, case limits)
- Coordinate build components (physical + electrical + logical)
- Base recommendations on real community experience - not on manufacturer advertising

The project is aimed at:
- Power users
- Hardware nerds
- IT system experts
- OS enthusiasts
- Anyone who *doesn't just want “FPS number X ”*, but wants to understand *why* something works - or doesn't.

---

## Planned main functions (modular implementation possible)

### PSU calculator 2.0
- Real consumption data (not just TDP)
- Takes into account peaks, OC, drives, RGB, USB, pumps, fans, etc.
- Safety margin & rail check

### Compatibility check (beyond “fits in”)
- Case → GPU collision check
- RAM height vs. cooler
- Fan placement vs. radiators

### Airflow & thermals
- Simplified heat zone model
- Recognize case-related bottlenecks

### Real-world data import
- Optional uploads from HWInfo/OpenHardwareMonitor
- GDPR-compliant anonymized
- Statistically usable → Community median formation

### Build scoring
- Evaluation in stability, efficiency, longevity, volume
- No “top X product”, but real, data-based recommendations

---

## Technical concept (high-level)

| Area                    | Possible implementation                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| Database                | PostgreSQL / MongoDB (planned centralized, later possibly decentralized or with API) |
| Backend                 | Python (FastAPI), modular structure                                                  |
| GUI                     | optionally with Qt / Electron / Web-Frontend                                         |
| 3D-Visualization        | long-term via Three. js / Unity (optional)                                           |
| hardware data sources   | scraping, user upload, open APIs                                                     |
| energy profile module   | load profiles, OC zones, differentiate usage behavior                                |

---

##  Technical concept (high-level)

| Area | Possible implementation |
|-----------------------|--------------------|
| Database | PostgreSQL / MongoDB (planned centralized, later possibly decentralized or with API) |
| Backend | Python (FastAPI), modular structure |
| GUI | optionally with Qt / Electron / Web-Frontend |
| 3D-Visualization | long-term via Three. js / Unity (optional) |
| hardware data sources | scraping, user upload, open APIs |
| energy profile module | load profiles, OC zones, differentiate usage behavior |

---

## Foreseeable challenges

| Problem | Remark |
|--------|-----------|
| Availability of accurate hardware models | Many custom designs (e.g. MSI vs. Gigabyte) with different consumption |
| Community upload & validation | Needs trust, GDPR compliance & good UX |
| Price query & stock level | Regionally different, scraping complex, possibly APIs necessary |
| Thermal model | Only roughly realistic to implement without CFD - but better than nothing |
| Ongoing costs | Database hosting, storage for uploads, possibly web front-end server |

# Rough cost idea

| Component | Estimated | Note |
|------------------|---------------|----------------------------------|
| Server & DB | ~5-15€/month | e.g. Hetzner/Contabo/VPS |
| Upload storage | ~1-5€/month | only on activation |
| Domain + TLS | ~10€/year | Optional |
| Traffic + API | varies | Depending on the number of users |

> A proof-of-concept can run 100% locally and free of charge.

---

## Values & Philosophy

- 100% Open Source & FOSS**
- No advertising, no paywall, no tracking
- Community-centered: Contributions welcome
- Transparency about every recommendation
- Data protection has priority - upload = always opt-in

---

## Funding ideas (if desired)

- Donations (e.g. via Liberapay, OpenCollective)
- Funding from FOSS foundations (e.g. NLnet, Sovereign Tech Fund)
- Partnerships with educational projects, hackspaces or universities
- **No** classic investors or feature locks

---

## Who should feel addressed?

- Developers who are interested in a realistic tech project
- People who are interested in low-level logic instead of buzzword builds
- Designers who want to think about the user experience
- Nerds with HWInfo logs

---

## Status

🟡 **Idea phase. No code yet. Vision only.

If you find this vision exciting:  
→ **Feel free to fork, discuss, implement, change, improve.** 
→ Author has *no vested interests*. Only passion for good tools.

---

## Long-term OEM participation (optional, but welcome)

Manufacturers and dealers can support RealBuild on several levels:

- Provision of technical data (dimensions, TDP, power profiles)
- Validation of database entries
- Upload of 3D models or compatibility data
- Co-financing of infrastructure (only voluntary, without influence)
- Cooperation for tool integration in own support

→ Goal: Win-win between transparency, support relief and better user experience

---

## Contact & License

- Author: *"SilverHaze99/InfoSecFor (project idea, concept) "*
- License: Apache 2.0 (FOSS compatible)

RealBuild is published under the **Apache 2.0 license**.

This means:
- Freely usable, modifiable, distributable
- Also allowed for commercial tools and OEM integrations
- No license fees or attribution required (but welcome)
- Patent and legal protection integrated

**"This project should live - not belong to me.  
If you want to use it, do it. If you want to make it better, make it even better. "**
