# **TAMMETRY MARKDOWN LINTER SPEC v1.0**  
*Formatting Invariants for the Civilisation‑Stack Knowledge Substrate*

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
This specification defines the canonical Markdown rules
that all files in the Tammetry notes repository must obey.
These rules ensure structural continuity, narrative coherence,
and deep‑time durability across the entire civilisation‑stack.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

# **1. Header Rules**

- **Header hierarchy** must be strictly sequential.  
  Allowed transitions: `# → ## → ### → ####`.  
  Forbidden: `# → ###`, `## → ####`, etc.
- Only **one** `#` header per file.
- Headers must be followed by **exactly one blank line**.
- No trailing punctuation in headers.

**Lint rule:**  
```
ERROR if header levels skip.
ERROR if multiple H1 headers exist.
ERROR if blank line missing after header.
```

---

# **2. Spacing Rules**

- Exactly **one blank line** between paragraphs.
- Exactly **one blank line** after lists, code blocks, and diagrams.
- No double blank lines except between major sections.
- No trailing whitespace on any line.

**Lint rule:**  
```
ERROR for >1 consecutive blank lines (except section breaks).
ERROR for trailing whitespace.
```

---

# **3. Banner Rules**

- Banners must use the canonical glyph:
  ```
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ```
- Banners may appear:
  - at the top of the file  
  - between major sections  
- Banners must be **full‑width**, **unbroken**, and **not indented**.

**Lint rule:**  
```
ERROR if banner uses non‑canonical glyphs.
ERROR if banner is indented or truncated.
```

---

# **4. Code Fence Rules**

- All code blocks must use triple backticks.
- Language tag optional but must be correct if present.
- No nested backticks inside code fences.
- No indentation before opening or closing fences.

**Lint rule:**  
```
ERROR if code fence indentation > 0.
ERROR if nested backticks detected.
ERROR if mismatched opening/closing fences.
```

---

# **5. List Rules**

- Unordered lists must use `-` exclusively.
- Ordered lists must use `1.` for every item (GitHub auto‑numbers).
- Nested lists must be indented by **4 spaces**.
- No mixing `*` and `-`.

**Lint rule:**  
```
ERROR if list markers inconsistent.
ERROR if nested list indentation != 4 spaces.
```

---

# **6. Diagram Rules**

- All diagrams must be inside fenced code blocks.
- Only spaces allowed — no tabs.
- Tree diagrams must use:
  - `├──`
  - `└──`
  - `│`

**Lint rule:**  
```
ERROR if diagram contains tabs.
ERROR if tree glyphs are inconsistent.
```

---

# **7. Link Rules**

- Internal links must be **relative paths**.
- External links must use **HTTPS**.
- Guided Links allowed only in narrative text.
- No links inside code fences.

**Lint rule:**  
```
ERROR if HTTP link detected.
ERROR if absolute internal path used.
ERROR if link appears inside code block.
```

---

# **8. Terminology Rules**

All documents must use the canonical civilisation‑stack lexicon:

- **Continuity Foundations**  
- **Continuity Bytecode**  
- **Continuity VM**  
- **Continuity Kernel**  
- **Continuity Runtime**  
- **Continuity OS**  
- **Continuity Graph**  
- **Continuity Projection**  
- **GLIRL**  
- **TRU**  
- **Civilisation‑Stack**  
- **Deep‑Time**  
- **Sovereignty**

**Lint rule:**  
```
WARNING if non‑canonical synonyms detected.
```

---

# **9. File Structure Rules**

Each `.md` file must follow:

1. Banner  
2. Title  
3. Overview  
4. Sections  
5. Optional appendix  

**Lint rule:**  
```
ERROR if file missing top banner.
ERROR if file missing overview section.
```

---

# **10. Tone Rules**

- Mythic‑technical  
- Declarative  
- Layered  
- Civilisational  
- No emojis  
- No conversational filler  

**Lint rule:**  
```
WARNING if emojis detected.
WARNING if conversational tone detected.
```

---

# **11. Continuity Rules (Meta‑Lint)**

Markdown must preserve:

- **identity continuity** (stable filenames)  
- **provenance continuity** (clean commit history)  
- **invariant continuity** (rules obeyed)  
- **narrative continuity** (sections flow logically)  
- **layer continuity** (trust → symbolic → civilisation)  
- **deep‑time continuity** (future readability guaranteed)

**Lint rule:**  
```
ERROR if file violates structural continuity.
WARNING if narrative flow inconsistent.
```
