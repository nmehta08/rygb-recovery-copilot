# RYGB Recovery Copilot

A clinician-facing prototype for organizing and interpreting the first 60 days of recovery after Roux-en-Y gastric bypass.

## The Idea

Postoperative information is usually scattered across operative notes, vital signs, laboratory results, nursing documentation, follow-up visits, medication lists and patient-reported symptoms.

The RYGB Recovery Copilot explores a different interface.

Instead of presenting postoperative information as isolated data points, the system organizes the patient's course as a longitudinal recovery story:

**What was the patient's baseline?**

**What happened during surgery?**

**What has happened since surgery?**

**What is changing?**

**What no longer fits the previous recovery pattern?**

**What clinically relevant information is missing?**

The core concept is that postoperative recovery should be interpreted as a trajectory rather than a collection of individual measurements.

---

## MVP Scope

The initial prototype focuses exclusively on patients undergoing Roux-en-Y gastric bypass during approximately the first 60 postoperative days.

Recovery is organized around four clinical domains:

1. Vital signs and postoperative complication surveillance
2. Weight and anthropometric trajectory
3. Nutrition, laboratory status and hydration
4. Symptoms, function and patient experience

The interface then places those domains into a longitudinal timeline.

---

## Why This Is Different From a Risk Calculator

Traditional risk tools typically follow a structure such as:

`Patient Variables → Mathematical Model → Risk Score`

The long-term concept behind RYGB Recovery Copilot is different:

`Patient History → Operation → Postoperative Events → Changing Patient State → Clinician Interpretation`

The goal is not simply to estimate whether a complication will occur.

The system is designed around understanding whether the patient's actual recovery remains consistent with their evolving clinical course.

A potentially important signal is therefore not simply:

> Nausea present

but:

> Nausea improved during the first postoperative week and has now worsened while oral fluid intake is declining.

The temporal relationship between events may carry more clinical meaning than the individual observations alone.

---

## Prototype Features

### Longitudinal Clinical Story

Condenses the patient's preoperative state, operative course and postoperative events into a concise recovery narrative.

### Recovery Timeline

Displays clinically meaningful events chronologically from preoperative assessment through the first two postoperative months.

### Four-Domain Assessment

Organizes postoperative information into:

- physiologic and surgical surveillance
- weight trajectory
- nutrition and hydration
- symptoms and patient experience

### Clinical Signals

Highlights meaningful changes in recovery patterns.

Signals describe observations or changes. They are not diagnoses.

### "What Doesn't Fit?"

A prototype clinical reasoning interaction designed to identify aspects of the current recovery course that appear discordant with the patient's previous trajectory.

### "What Changed?"

Reconstructs meaningful changes over time rather than simply displaying the latest measurement.

### "What Is Missing?"

Explicitly identifies important unavailable information instead of assuming or fabricating missing clinical facts.

### Rapid Clinical Summary

Produces a short surgeon-facing reconstruction of the patient's current postoperative course.

---

## Current Technology

The current MVP is intentionally simple.

It consists of:

- `index.html`
- embedded CSS
- embedded JavaScript
- synthetic patient information
- deterministic rule-based demonstration logic

There is no backend.

There is no database.

There is no external API.

There is currently no artificial intelligence model.

This allows the clinical workflow and interface concept to be evaluated before introducing additional technical complexity.

---

## Future Architecture

A future version could potentially incorporate:

`EHR data`

↓

`Preoperative patient state`

↓

`Operative and anesthesia information`

↓

`Postoperative clinical data`

↓

`Patient-reported information`

↓

`Longitudinal patient state model`

↓

`Explainable clinical reasoning interface`

Potential future capabilities could include retrieval of relevant historical information, temporal trend recognition, source-linked clinical summaries, patient-specific recovery modeling and identification of clinically meaningful deviations from expected recovery.

Any predictive or clinical decision-support functionality would require appropriate clinical validation, safety evaluation and regulatory assessment before clinical deployment.

---

## Design Principle

The central design principle is simple:

> **Recovery is a story unfolding over time.**

The prototype attempts to make that story easier for clinicians to see.

---

## Clinical Safety

This repository contains a research and design prototype only.

It is not a medical device.

It is not intended to diagnose disease, recommend treatment, replace clinician judgment or guide the care of real patients.

All patient information included in the demonstration should be synthetic.

No protected health information should be added to the public prototype.

Any future clinical implementation would require appropriate privacy, security, validation, institutional governance and regulatory review.

---

## Status

**Stage:** Early MVP / concept demonstration

**Initial procedure:** Roux-en-Y gastric bypass

**Initial observation window:** Approximately 60 postoperative days

**Current intelligence layer:** Rule-based demonstration

**Future direction:** Longitudinal clinical reasoning and recovery-state modeling

---

## Vision

The longer-term vision is not to build another surgical risk calculator.

It is to explore whether software can maintain an understandable, continuously evolving representation of a surgical patient's recovery and help clinicians rapidly answer:

**What happened?**

**What changed?**

**What matters now?**

**What doesn't fit?**

**What information do I still need?**
