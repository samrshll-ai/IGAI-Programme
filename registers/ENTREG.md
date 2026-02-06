# ENTREG — Entity Register (Bootstrap Version)
**Version:** 0.1.0  
**Status:** Draft  
**Scope:** Programme‑wide  
**Purpose:** To establish the canonical register of entity types recognised by the Programme’s ontology.

---

## 1. ENTITY
**Code:** ENTITY  
**Type:** Meta‑entity  
**Version:** 0.1.0  
**Status:** Active  

### Definition
An entity is a real‑world thing about which the business needs to hold information.  
An entity is a class of real‑world objects represented in a metadata registry.

### Derivation
Derived from SSADM v4.2 Logical Data Structure and ISO/IEC 11179 Metadata Registry, which together provide the historic conceptual foundation and the current authoritative framework.

### Description
An ENTITY exists within a Logical Data Structure (LDS), which describes the relationships between entities and the business meaning of those relationships. ENTITY is the root metadata type within the Programme’s LDS. It defines the structural and semantic characteristics of all entity types recorded in ENTREG. Every entity type in the Programme, including ENTITY itself, is an instance of this definition.

### Purpose
To provide a consistent, governed, and extensible framework for defining the types of things that exist within the Programme’s ontology, including their attributes and their participation in relationships defined within the LDS.

### Attributes
(Each represented using ATTRIBUTE instances)

- **Entity_Name** — Unique name identifying the entity type.  
- **Definition** — The authoritative definition of the entity type.  
- **Description** — Contextual explanation of the entity type.  
- **Attributes** — Governed list of ATTRIBUTE instances defining the internal structure of the entity type.  
- **Version** — Semantic version of the entity type definition.  
- **Status** — Lifecycle state (Active, Deprecated, Superseded).  
- **Created_On** — Timestamp of initial creation.  
- **Updated_On** — Timestamp of most recent update.

### Notes
ENTITY is self‑describing. Its own definition is expressed using the same structure it imposes on all other entity types. This provides a stable, recursive foundation for the Programme’s ontology and ensures that ENTREG can represent itself without special‑case logic.

## 2. ATTRIBUTE

**Name:** ATTRIBUTE  
**Version:** 0.1.0  
**Timestamp:** 2026/02/06 Fri 14:40 GMT  
**Register:** ENTREG  
**Status:** Bootstrap Version  
**Author:** IGAI Programme  

### Definition  
An ATTRIBUTE is a fundamental unit of descriptive data that expresses a single property, characteristic, or quality of an ENTITY. It is atomic and cannot be decomposed further within the Logical Data Structure. It provides the semantic detail needed to distinguish, classify, or describe instances of an ENTITY.

### Purpose  
The purpose of an ATTRIBUTE is to define the internal structure of an ENTITY by specifying the discrete pieces of information that describe it. Attributes enable consistent representation, validation, comparison, and interpretation of entity instances across the Programme.

### Properties  
- **Atomicity:** Represents a single, indivisible concept.  
- **Name:** Unique within the scope of its ENTITY.  
- **Datatype:** The form of value the ATTRIBUTE may take (e.g., text, number, date, boolean).  
- **Cardinality:** Specifies whether the ATTRIBUTE may occur once or multiple times.  
- **Optionality:** Determines whether the ATTRIBUTE must be present for an ENTITY instance to be valid.  
  - **Mandatory:** Must have a non‑null value for the ENTITY instance to be valid.  
  - **Optional:** May be null; the ENTITY instance remains valid without a value.  
- **Domain:** The permitted set of values or constraints governing valid instances.  
- **Description:** A human‑readable explanation of the ATTRIBUTE’s meaning and role.

### Constraints  
- An ATTRIBUTE must belong to exactly one ENTITY.  
- An ATTRIBUTE must have a defined datatype.  
- An ATTRIBUTE must have a unique name within its ENTITY.  
- An ATTRIBUTE must not duplicate the meaning of another ATTRIBUTE within the same ENTITY.  
- An ATTRIBUTE’s meaning must remain stable across versions.  
- Optionality must be explicitly defined and must not change without versioning.

### Notes  
- ATTRIBUTE definitions form the backbone of the Logical Data Structure (LDS).  
- Optionality is a semantic property, not an implementation detail.  
- ATTRIBUTE definitions must remain independent of implementation technologies.  
- ATTRIBUTE definitions should support long‑term interpretability and auditability.
