# **FORMATTING INVARIANTS — TAMMETRY MARKDOWN SPEC v1.0**

These invariants define the **canonical Markdown style** for the entire civilisation‑stack notes repository.  
Every `.md` file must satisfy these invariants to preserve:

- structural continuity  
- narrative continuity  
- readability continuity  
- deep‑time durability  

---

## **1. Header Invariants**
- **Header hierarchy** must be strictly monotonic.  
  No skipping levels (e.g., `#` → `###` is forbidden).
- Top‑level header (`#`) appears **once** per file.
- Section headers use `##`.
- Subsections use `###`.
- No deeper than `####` unless absolutely required.

**Invariant:**  
```
∀ headers: level(n+1) ⇒ parent(level n)
```

---

## **2. Spacing Invariants**
- Exactly **one blank line** after every header.
- Exactly **one blank line** between paragraphs.
- No trailing spaces.
- No double blank lines except to separate major sections.

**Invariant:**  
```
Spacing = 1 everywhere except section boundaries.
```

---

## **3. Banner Invariants**
- Banners use **full‑width unicode lines**:
  ```
  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ```
- Banners must appear **only**:
  - at the top of the file  
  - optionally between major sections  
- Banners must be **symmetrical** and **unbroken**.

**Invariant:**  
```
Banners are structural, not decorative.
```

---

## **4. Code Fence Invariants**
- All code blocks use triple backticks:
  ```
  ```text
  ```
- Language tag optional; if used, must be correct.
- No nested backticks inside code fences.
- No indentation before fences.

**Invariant:**  
```
Code fences must be atomic and unambiguous.
```

---

## **5. List Invariants**
- Lists must use `-` for unordered items.
- Lists must use `1.` for ordered items.
- Nested lists must be indented by **4 spaces**.
- No mixing `*` and `-`.

**Invariant:**  
```
List syntax must be uniform across the entire repo.
```

---

## **6. Diagram Invariants**
- All diagrams must be **monospace‑aligned**.
- Diagrams must be wrapped in code fences.
- No tabs — only spaces.
- Tree diagrams must use consistent glyphs:
  - `├──`
  - `└──`
  - `│`

**Invariant:**  
```
Diagrams must render identically in GitHub, VS Code, and plain text.
```

---

## **7. Link Invariants**
- Internal links must be relative paths.
- External links must use HTTPS.
- Guided Links may appear in narrative text but **never** inside code fences.

**Invariant:**  
```
Links must be stable across hosts and epochs.
```

---

## **8. Terminology Invariants**
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

**Invariant:**  
```
Terminology must be consistent across all layers.
```

---

## **9. File Structure Invariants**
Each `.md` file must follow:

1. Banner  
2. Title  
3. Overview  
4. Sections  
5. Optional appendix  

**Invariant:**  
```
Every file is a self‑contained artefact.
```

---

## **10. Tone Invariants**
- Mythic‑technical  
- Declarative  
- Layered  
- Civilisational  
- No conversational filler  
- No emojis  

**Invariant:**  
```
Tone must reflect the civilisation‑stack identity.
```

---

# **11. Continuity Invariants for Markdown**
Markdown itself must preserve:

- **identity continuity** (file names stable)  
- **provenance continuity** (commit history clean)  
- **invariant continuity** (formatting laws obeyed)  
- **narrative continuity** (sections flow logically)  
- **layer continuity** (trust → symbolic → civilisation)  
- **deep‑time continuity** (future readability guaranteed)  

**Invariant:**  
```
Markdown is part of the trust‑continuity system.
```
