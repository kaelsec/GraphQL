# Vendor-Agnostic Native GraphQL Security Standard (v1.1)

A practitioner-driven security standard that defines **GraphQL-native security risks and baselines**,  
independent of vendors, frameworks, or specific implementations.

This document focuses on **structural security properties of GraphQL** — not generic web vulnerabilities —
and provides **actionable, testable security baselines** for modern GraphQL systems, including Federation.

---

## 🎯 Purpose

GraphQL is not REST.

Its security model is fundamentally different due to:
- Client-controlled query shape and execution cost
- Resolver-level authorization
- Graph traversal–based data access
- Single endpoint architecture
- Federated trust delegation (Gateway ↔ Subgraph)

This standard defines:
- **Native threat models** specific to GraphQL
- **Structural weaknesses** that cannot be addressed by REST-oriented controls
- **Security baselines** aligned with real-world GraphQL execution semantics
- **Verification-oriented test cases** usable in CI/CD pipelines

---

## 📌 Scope

### In Scope
- Schema Design
- Resolver Authorization Logic
- Query Parsing & Execution Safety
- Federation Gateway & Subgraph Trust Model

### Out of Scope
- OS / Network / Container hardening
- OAuth2 / OIDC protocol handshakes
- Database encryption or storage-layer security

---

## 🧠 Core Concepts

This standard formalizes four **GraphQL-native structural risks**:

1. **Recursive Resource Exhaustion**  
   Exponential execution cost via deep or cyclic graph traversal

2. **Authorization Context Fragmentation**  
   Field-level access control inconsistencies across resolver chains

3. **Transport Amplification**  
   Query batching and multi-operation abuse bypassing rate limits

4. **Distributed Trust Fragility (Federation)**  
   Implicit trust assumptions between Gateway and Subgraphs

---

## 🛡️ What This Is (and Is Not)

**This is:**
- A vendor-agnostic security baseline
- Compatible with Apollo, Hasura, GraphQL Yoga, custom engines
- Designed for AppSec, DevSecOps, and platform teams
- Aligned with OWASP ASVS and GraphQL Cheat Sheet

**This is NOT:**
- A vulnerability list
- A scanner
- A framework-specific hardening guide

---

## 🧪 Security Testing Alignment

The document includes:
- An **Attack Pattern Matrix**
- Reproducible PoC-style test cases
- CI/CD-friendly validation goals

This allows teams to move from:
> *“We should secure GraphQL”*  
to  
> *“We can prove this GraphQL system enforces security invariants.”*

---

## 🔗 Standards Alignment

- OWASP ASVS (V4 / V5)
- OWASP GraphQL Cheat Sheet
- Apollo & Hasura Security Practices
- NIST 800-204B (Microservices Security)

---

## 📄 Document

- [`Vendor-Agnostic_Native_GraphQL_Security_Standard_v1.1.md`](./Vendor-Agnostic_Native_GraphQL_Security_Standard_v1.1.md)

---

## 🧭 Status

This is a **living document**.  
Feedback, issues, and practitioner insights are welcome.

The goal is not formal standardization first,  
but **shared understanding and practical convergence**.

---

## 📜 License

This document is provided for public use and discussion.
No warranty is provided. Use at your own risk.
