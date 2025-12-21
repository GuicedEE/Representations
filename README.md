# 🧱 GuicedEE Representations

[![JDK](https://img.shields.io/badge/JDK-25%2B-0A7?logo=java)](https://openjdk.org/projects/jdk/25/)
[![Build](https://img.shields.io/badge/Build-Maven-C71A36?logo=apachemaven)](https://maven.apache.org/)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

DDD-friendly representation interfaces and value abstractions shared across GuicedEE modules.

## ✨ Features
- Value objects and representation interfaces for consistent DTOs and messages
- Topic-first naming that aligns with project glossaries
- Immutable-by-default patterns recommended for safety

## 📦 Install (Maven)
```
<dependency>
  <groupId>com.guicedee</groupId>
  <artifactId>guiced-representations</artifactId>
</dependency>
```

## 🚀 Quick Example (Value Object)
```
public record EmailAddress(String value) {
  public EmailAddress {
    if (value == null || !value.contains("@")) throw new IllegalArgumentException("invalid email");
  }
}
```

## 📚 Docs & Rules
- Rules: `RULES.md`
- Guides: `GUIDES.md`
- Architecture: `docs/architecture/README.md`

## 🤝 Contributing
- Issues/PRs welcome. Use glossary-aligned names and keep docs updated.

## 📝 License
- Apache 2.0 — see `LICENSE`.
