# BIMCapabilities

Open-source ecosystem of reusable BIM validation, correction, and optimization capabilities.

Build automation through configuration, not custom code.

---

## Vision

Most BIM organizations repeatedly solve the same problems:

* Missing shared parameters
* Naming violations
* Family quality issues
* Template inconsistencies
* Coordination rule violations

Traditional automation creates custom code for every rule.

BIMCapabilities takes a different approach.

Instead of:

```text
Knowledge
+
Custom Validator
+
Custom Fixer
```

BIMCapabilities promotes:

```text
Knowledge
+
Configuration
+
Reusable Capability
```

The goal is to allow hundreds of organizational rules to be implemented through a small set of reusable, open-source capabilities.

---

## Core Principle

```text
Capability
+
Configuration
=
Automation
```

Capabilities provide generic behavior.

Configuration provides organizational intent.

Knowledge remains the source of truth.

---

## Architecture

```text
Knowledge
    ↓
Configuration
    ↓
Capability
    ↓
Engine
    ↓
Execution
    ↓
Report
```

Capabilities are reusable operations.

Configurations bind capabilities to organizational rules.

---

## Example

Organizational rule:

```text
All Door families must contain MY_FireRating.
```

Configuration:

```json
{
  "engine": "parameter-engine",
  "capability": "HasSharedParameter",
  "parameter": "MY_FireRating"
}
```

Execution:

```text
Parameter Engine
    ↓
HasSharedParameter
    ↓
Validation Result
```

No custom code required.

---

## Available Engines

### Parameter Engine

Capabilities:

* Exists
* Missing
* HasValue
* Equals
* NotEquals
* GreaterThan
* LessThan
* MatchesRegex
* HasSharedParameter

---

### Naming Engine

Capabilities:

* StartsWith
* EndsWith
* MatchesPattern
* ContainsToken
* MissingToken
* ForbiddenToken

---

### Family Quality Engine

Capabilities:

* HasImportedCAD
* DuplicateTypes
* ExcessParameters
* MissingConnectors
* OversizedFamily

---

### Template Engine

Capabilities:

* TemplateExists
* FilterExists
* ScheduleExists
* BrowserRuleExists

---

### Coordination Engine

Capabilities:

* GroupClashes
* ScoreSolution
* ValidateRule
* RankOptions
* DetectException

---

## Open Source Model

BIMCapabilities is open source.

The repository contains:

* Engine source code
* Capability implementations
* Documentation
* Tests
* Examples
* Configuration schemas

The repository does not contain:

* Company knowledge
* Customer standards
* Project data
* Evidence
* Reports

---

## Ownership Model

### Open Source

* Engines
* Capabilities
* Documentation
* Tests
* Schemas

### Organization-Owned

* Knowledge Base (KB)
* Validation Configurations (VAL)
* Fix Configurations (FIX)
* Evidence
* Reports
* Standards
* Exceptions

---

## Design Philosophy

Knowledge should be reusable.

Automation should be configurable.

Custom code should be rare.

The preferred path is:

```text
New Knowledge
    ↓
New Configuration
```

not:

```text
New Knowledge
    ↓
New Validator
    ↓
New Fixer
```

---

## Relationship to BIMLinker

BIMCapabilities is the open-source capability ecosystem.

BIMLinker is the organizational learning platform that can consume these capabilities.

```text
BIMCapabilities
    ↓
Reusable Capabilities

BIMLinker
    ↓
Knowledge
Validation
Fixes
Reports
AI Assistance
Organizational Learning
```

The two projects are designed to work together but can evolve independently.

---

## Long-Term Goal

Create a shared ecosystem of reusable BIM capabilities that enables organizations to transform knowledge into validation, correction, and optimization workflows without continuously creating custom automation code.

```text
Knowledge
    ↓
Configuration
    ↓
Capability
    ↓
Execution
```

Build automation through configuration, not custom code.

