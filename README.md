# Aura Plant — An Ambient Companion that Grows with You

## 🧠 Concept and Motivation

Aura Plant is an ambient digital wellbeing companion that visualises daily habits through the metaphor of a living plant. Rather than presenting health data through numerical dashboards, wellbeing is communicated through colour and light behaviour — designed to feel more emotionally engaging and less cognitively demanding than typical tracking apps.

The product targets individuals living alone, particularly international students in small accommodation spaces, where movement routines and sleep patterns can easily become irregular. Animal metaphors were considered early on (inspired by pet restrictions in student housing) but dropped, since emotional attachment to animals varies across cultures — a plant is a more neutral, widely understood symbol of growth and care.

Unlike wearables (Apple Watch, Fitbit, Oura) that turn users into passive data generators, Aura Plant combines sensed activity with ambient feedback to keep reflection — not accumulation — at the centre of the experience.

---

## 🌱 Interaction Behaviour

The system operates across three states — **Indoor**, **Outdoor**, and **Sleep** — with movement sensing and button input translating user behaviour into light-based feedback. The interaction model prioritises visibility and clarity over numerical tracking.

---

## 🛠️ Technologies Used

- **Micro:bit** – core sensing and control logic
- **Ultrasonic sensor** – movement detection (replacing an earlier PIR sensor approach)
- **NeoPixel LED ring** – ambient colour feedback
- **LCD display** – mode state transparency (Indoor / Outdoor / Sleep)
- **Extension board** – wiring integration for all components

---

## 🧩 What Didn't Work (and What Replaced It)

Several early approaches were tested and dropped based on real hardware constraints:

1. **Light exposure sensing** — intended to track daylight intake, but the micro:bit's light sensor couldn't distinguish natural sunlight from artificial lighting, and the lack of a built-in real-time clock made time-based logic unreliable. Removed to avoid misleading feedback.
2. **PIR motion sensors** — too sensitive, picking up general heat variation rather than meaningful movement.
3. **Ultrasonic sensing (adopted)** — detects distance change over time, with thresholds tuned to distinguish large-body motion from minor gestures.
4. **Inconsistent sensor readings** — initially assumed to be a software bug, several rounds of debugging followed before the real cause was found: overlapping pin allocations across components causing interference. Reassigning pins resolved it.
5. **Button wiring** — breadboard-based integration (the only method covered in workshop guidance) became impractical once the design moved to a compact enclosure. External research revealed the correct diagonal pin connections needed to complete the circuit.
6. **Soldering vs. taping** — soldering the button connections wasn't pursued due to limited tool access, so taping was used instead as a non-permanent fastening method — a decision that later introduced real constraints during reassembly (see Limitations).

---

## 🪴 Physical Prototyping

- **Flower petals**: pipe-cleaner construction was tested first but rejected — the material was too dense and blocked LED light diffusion. White baking paper was used instead for its translucency.
- **Stem**: built from a kitchen roll tube (for height and a hollow interior to hide wiring), reinforced externally with straws and superglue.
- **Enclosure**: a transparent plastic container was tried first but discarded — it exposed internal wiring and looked visually cluttered, undermining the ambient design intent. A cardboard enclosure (painted black for contrast and a cleaner finish) replaced it, with custom cut-outs for the LCD, sensor, and button.

---

## 🎯 Key Contributions

- Designed and built the physical prototype, including material selection and enclosure iteration
- Diagnosed and resolved a hardware pin-conflict issue affecting sensor reliability
- Integrated ultrasonic sensing, NeoPixel feedback, and LCD state display into a single working system

---

## ⚠️ Limitations

- Baking paper (light diffuser) lost structural integrity over time, causing deformation
- Glue-stick adhesive weakened, leading to components detaching after extended use
- Button connections were taped rather than soldered, due to limited tool access — a decision that made later reassembly and stabilisation significantly more time-consuming
- Continuous USB power was required, as the NeoPixel ring at full brightness exceeded stable battery capacity
- At the prototype stage, wellbeing states were simulated from direct sensor triggers rather than the longer-term behavioural pattern modelling the real product would need

---

## 🌿 Future Improvements

- More durable materials (translucent acrylic or 3D-printed diffusers) for structural stability and better light quality
- Reintroducing light sensing with a more reliable method to distinguish natural sunlight from artificial lighting
- Incorporating evidence-based wellbeing metrics (sleep duration, activity levels, sunlight exposure) for more meaningful, pattern-based feedback rather than immediate sensor triggers
- Expanding the LCD into a reminder-based interface, combining ambient feedback with contextual prompts

---

## 📄 Project Report

This report provides a full explanation of the design process, technical build, and evaluation, including figures showing the system interaction flow, electronics integration, and prototype iterations.

[View Full Report](#) <!-- replace with your PDF link once uploaded -->
