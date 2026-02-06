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
