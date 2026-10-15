# AmbeGo - Unified Ambulance Booking & Emergency Response Platform

AmbeGo is a unified ambulance aggregator and emergency transportation platform connecting patients, public emergency programs (108/112), hospital critical care units, and certified private operators through an Ola/Uber-style dispatch engine.

---

## 🚑 Key Differentiators & Features

### 1. Unified Multi-Provider Aggregation
- **Category 1: Public & Government Services**: Subsidized/Free 108 Emergency Response (GVK-EMRI) with standardized BLS & ALS support.
- **Category 2: Private Ambulance Services**: Express fleets (Medulance, Falcon) with high cabin amenities and priority dispatch.
- **Category 3: Hospital Fleets**: Direct-admit Mobile Intensive Care Units (Apollo, Manipal, Fortis) with real-time ER bed integration.
- **Category 4: Any Eligible Provider**: Intelligent aggregator mode scanning all providers for the fastest road arrival ETA.

### 2. Category-Specific Ambulance Package Tiers
- **Premium / Luxury**: Smooth air-suspension glide cabin, climate control, motorized hydraulic gurney, dual oxygen lines, and family companion seating.
- **Semi-Premium**: Air-conditioned patient compartment, verified medical oxygen, and ergonomic roll-in stretcher.
- **Basic**: Essential patient transport, folding stretcher, and certified first-aid equipment.

### 3. Medical Equipment & Capability Customization
- Oxygen equipment (gauge pressure in PSI and prescribed flow rate in L/min).
- Basic Life Support (BLS) & Advanced Life Support (ALS) with defibrillator & cardiac telemetry.
- Mobile ICU with portable mechanical ventilators and arterial blood gas monitoring.
- Wheelchair lift & motorized zero-jolt loading stretchers.

### 4. Two-Stage Real-Time Navigation
- **Stage 1 (Ambulance to Patient)**: Live vehicle GPS tracking, heading rotation, route polyline, and crew calling.
- **Stage 2 (Patient to Hospital)**: Real-time emergency transit to hospital emergency bay with pre-alert notification to receiving ER.

### 5. Four Connected User Experiences
- **Patient & Family Application**: Instant booking, provider/ETA comparison, 2-stage tracking, SOS family broadcast, and emergency fallback to 112/108.
- **Ambulance Driver Application**: High-contrast driver dashboard, incoming request countdown timer (20s), turn-by-turn navigation handoff, and sequential trip status updates.
- **Ambulance Provider Portal**: Fleet management, vehicle onboarding, driver roster, certification tracking, and base/per-km pricing rules.
- **Platform Admin & Dispatch Dashboard**: Network SLA monitoring, active dispatches, compliance audits, and unassigned request escalation matrix.

### 6. Procedural Three.js 3D Ambulance & Medical Cabin Inspector
- 10-part composite procedural 3D model (cab, chassis, siren lightbars with red/blue strobes, wheels with rubber tires/alloy rims, hydraulic patient stretcher, dual oxygen cylinders, ECG vital monitor with animated waveforms, and IV drip stand).
- Studio PBR lighting with `RoomEnvironment` PMREM reflections, ACESFilmic tone mapping, warm key light, and contact shadow grounding.
- Damped camera controls and collapsible bottom control dock with exploded-view cabin slider.

### 7. Gemini Multimodal Intelligence
- **Voice Dispatch Assistant**: Real-time conversation triage simulator with `gemini-3.8-live`.
- **Search Grounding**: Live regional road delays and ER wait-time telemetry using `gemini-3.8-flash` with Google Search.
- **High-Thinking Clinical Triage**: Complex multi-factor transport decision engine with `gemini-4-argon` and `thinkingLevel: HIGH`.
- **Rapid First-Aid Guidance**: Low-latency bystander CPR and airway instructions via `gemini-3.1-flash-lite`.
- **Multi-Turn Emergency Copilot**: Reassuring clinical advisor for patients and relatives.

### 8. Bioscience Clinical Calculations
- **Glasgow Coma Scale (GCS)**: Eye (1-4), Verbal (1-5), and Motor (1-6) scoring with triage routing.
- **Emergency Severity Index (ESI)**: Levels 1 through 5 triage determination.
- **Oxygen Cylinder Duration Calculator**: Exact clinical formula: `Duration (min) = (Pressure - Safe Residual) × Factor / Flow Rate`.

### 9. Google Workspace Contacts Integration
- Google People API OAuth integration (`contacts.readonly`) to import family members and emergency physicians.
- 1-Click SOS Broadcast transmitting live GPS tracking URL to emergency contacts.

---

## 🛠 Tech Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS, Three.js, Lucide Icons.
- **AI & Grounding**: `@google/genai` (gemini-3.8-flash, gemini-4-argon, gemini-3.1-flash-lite, gemini-3.8-live).
- **Authentication & OAuth**: Firebase Auth with Google Workspace People API.
- **Geospatial & Mapping**: Dynamic 2-Stage Navigation SVG Canvas with Google Maps Platform handoff.

---

## 🚀 Running the App

```bash
# Install dependencies
npm install

# Run the dev server
npm run dev

# Build for production
npm run build
```
