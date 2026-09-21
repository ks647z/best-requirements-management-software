# IEC 62304 software requirements starter

A structure for software requirements under IEC 62304, with safety classification, architecture linkage and problem resolution traced back to risk. It is a starting structure, not a compliance guarantee, and it is not a substitute for reading the standard.

Licensed CC BY 4.0 by [Matrix One](https://matrixone.health).

---

## 1. Software safety classification

IEC 62304 classifies each software system, and each software item within it, by the harm that a failure could cause.

| Class | Definition in the standard | Practical effect |
|-------|---------------------------|------------------|
| A | No injury or damage to health is possible | Lightest documentation set |
| B | Non serious injury is possible | Architecture, detailed design for items, unit verification |
| C | Death or serious injury is possible | Full set, including detailed design and verification of every software unit |

Classify the whole software system first, then classify items. An item may be classified lower than its parent only where segregation between items is documented and justified.

| Item ID | Software item | Class | Segregation rationale |
|---------|---------------|-------|-----------------------|
| SI-001 | Alarm module | C | |
| SI-002 | Reporting module | A | No data path to therapy delivery, documented in ARCH-003 |

## 2. Software requirements

Each software requirement traces up to a system requirement and down to an architecture item and a verification.

| ID | Requirement | Software item | Class | Traces up to | Architecture ref | Verification method | Test case | Status |
|----|-------------|---------------|-------|--------------|------------------|---------------------|-----------|--------|
| SWR-001 | The alarm module shall poll the reservoir sensor at 1 Hz. | SI-001 | C | SYS-001 | ARCH-002 | Test | TC-102 | Draft |
| SWR-002 | The alarm module shall raise ALM_LOW_RESERVOIR when three consecutive readings fall below the configured threshold. | SI-001 | C | SYS-001 | ARCH-002 | Test | TC-103 | Draft |

Requirement categories to work through, so that nothing is discovered at verification: functional behaviour, inputs and outputs, interfaces to other systems and to hardware, alarms and warnings, security and access control, data definition and retention, installation and acceptance, maintenance and decommissioning, user documentation, regulatory labelling driven behaviour.

## 3. Software architecture

| ID | Architecture item | Realises | Interfaces | Class | SOUP |
|----|-------------------|----------|------------|-------|------|
| ARCH-002 | Alarm service | SWR-001, SWR-002 | Sensor driver, UI event bus | C | No |

## 4. SOUP inventory

Software of unknown provenance has to be identified, justified and monitored for published anomalies.

| SOUP ID | Component | Version | Purpose | Manufacturer | Hardware and software requirements | Anomaly list reviewed | Risk assessment ref |
|---------|-----------|---------|---------|--------------|-----------------------------------|----------------------|---------------------|
| SOUP-001 | | | | | | | |

## 5. Risk control linkage

Risk controls implemented in software are software requirements, and their effectiveness has to be verified, not just their presence.

| Risk ID | Hazardous situation | Risk control | Implemented by | Verification of effectiveness | Residual risk accepted |
|---------|--------------------|--------------|----------------|-------------------------------|------------------------|
| RSK-012 | Delayed low reservoir alert leads to interrupted therapy | Audible alert within 2 seconds | SWR-001, SWR-002 | TC-102, TC-103 | |

## 6. Problem resolution

Every reported problem is evaluated for its risk impact and traced to the change that resolved it, and to the re verification that closed it.

| Problem ID | Description | Reported | Class impact | Risk re evaluated | Change request | Re verification | Closed |
|------------|-------------|----------|--------------|-------------------|----------------|-----------------|--------|
| PR-001 | | | | | CR-001 | TC-102 | |

## 7. Verification record

| Test case | Verifies | Method | Run date | Version under test | Result | Evidence ref |
|-----------|----------|--------|----------|--------------------|--------|--------------|
| TC-102 | SWR-001 | Test | | | | |

## 8. The thing to check before an audit

Pick one requirement at random. Walk it forward to a verification result and backward to a user need, and produce the risk analysis, the control, the evidence the control works, the design review that approved it, and what has changed since. If that takes more than a minute, the structure is fine and the tooling is the problem.
