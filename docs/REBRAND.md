# 📘 Detailed Rebrand & Maintenance Guide for `webpg2app`

## Objective
Take the original `Pake` repository and perform a full, safe rebrand and maintenance setup. The goal is to:

1. Rename all instances of `Pake` or `pake` to `webpg2app`.
2. Maintain all functionality and logic without breaking builds, CLI, or Tauri.
3. Add a permanent, minimal, faded watermark on all frontend pages with letters.
4. Restructure documentation and README files for clarity.
5. Set up guidelines for local development, CLI usage, and CI/CD pipelines.
6. Ensure the watermark is extremely difficult to remove, even for experienced developers or automated AI tools.
7. Provide professional recommendations for maintaining and extending the project.

---

## 1️⃣ Repository Rename Strategy

**Scope:**
- CLI commands (`pake`, `pake-cli`) → `webpg2app`, `webpg2app-cli`
- Rust crate names (`Cargo.toml`, `mod`, `use`) → `webpg2app`
- Tauri configuration (`productName`, `identifier`) → `webpg2app`
- Build scripts, npm/pnpm packages, rollup config → `webpg2app`
- Documentation (`README.md`, `README_CN.md`, `docs/*`) → `webpg2app`
- Tests (`tests/*`) → `webpg2app`
- GitHub Actions workflows → `webpg2app`
- Binary output names → `webpg2app.exe` / `webpg2app.app`

**Constraints:**
- Do not rename Rust internal modules unless required.
- Do not rename Cargo package IDs unless validated.
- Do not rename Tauri internal config keys without validation.

**Approach:**
1. Categorize occurrences of `pake` by CLI, Rust, Tauri, tests, docs, and workflows.
2. Perform renaming in layers:
   - Docs first (safe)
   - CLI second
   - Rust crate third
   - Tauri configs fourth
   - Workflows fifth
   - Build artifacts sixth
   - Tests last
3. Validate each layer before proceeding to the next.

---

## 2️⃣ CLI & Build Artifacts

**Rename:**
- CLI binary: `pake` → `webpg2app`
- CLI package: `pake-cli` → `webpg2app-cli`
- Documentation examples, usage guides, and help text updated.
- Build scripts and rollup outputs named `webpg2app`.

**Validation:**
- Ensure CLI commands execute correctly for URLs and names.
- Ensure builds produce functional desktop apps for macOS, Windows, Linux.

---

## 3️⃣ Tauri Configuration Updates

**Required Changes:**
- `productName`: `webpg2app`
- `identifier`: `com.webpg2app.app`
- Validate that changing identifier does not break auto-update (safe if using a fresh fork).

**Notes:**
- Maintain all Tauri options for window size, title bar, drag-and-drop, and shortcut behavior.
- Ensure style customization features are preserved.

---

## 4️⃣ Watermark Specification

**Text:** `mwakidenis`  
**Placement:** minimal space, fixed across all pages, bottom-right or unobtrusive area.  
**Opacity:** subtle (around 0.08).  
**Interaction:** non-clickable, non-selectable.  
**Security:** hidden enough to be extremely difficult to remove; should resist casual deletion and automated AI removal.

**Color Scheme (Alternate Black & Red):**
- m → Black  
- w → Red  
- a → Black  
- k → Red  
- i → Black  
- d → Red  
- e → Black  
- n → Red  
- i → Black  
- s → Red  

**Goal:** Each letter individually colored so that combined, the text alternates black and red smoothly, is minimally intrusive, and cannot be easily removed.

**Injection:** Should appear automatically on all frontend pages via the existing UI framework, without breaking existing JS, Rust, or Tauri logic.

**Snippet to Inject Watermark:**

```ts
// file: src/watermark.ts (or include in main frontend entry)
export function injectWatermark() {
  if (document.getElementById("wm-webpg2app")) return; // Prevent duplicates

  const text = "mwakidenis";
  const colors = ["black", "red"]; // Alternating colors
  const container = document.createElement("div");

  container.id = "wm-webpg2app";
  container.style.position = "fixed";
  container.style.bottom = "5px";
  container.style.right = "5px";
  container.style.opacity = "0.08";
  container.style.fontSize = "14px";
  container.style.pointerEvents = "none";
  container.style.userSelect = "none";
  container.style.zIndex = "9999";
  container.style.fontFamily = "sans-serif";

  for (let i = 0; i < text.length; i++) {
    const span = document.createElement("span");
    span.textContent = text[i];
    span.style.color = colors[i % colors.length]; // alternate black/red
    container.appendChild(span);
  }

  document.body.appendChild(container);
}

// Automatically inject on DOMContentLoaded
if (document.readyState === "loading") {
  document.addEventListener("DOMContentLoaded", injectWatermark);
} else {
  injectWatermark();
}
```

---

## 5️⃣ Documentation Restructuring

**Files to update:**
- README.md
- README_CN.md
- CONTRIBUTING.md
- AGENT.md
- CLAUDE.md
- Any docs in /docs folder

**Guidelines:**
- Replace all mentions of Pake → webpg2app.
- Include clear instructions for CLI usage, build, and dev setup.
- Add watermark description for developers.
- Organize sections for Features, Installation, Usage, Development, Testing, License, Contributors, and Support.
- Ensure SEO-friendly headings for discoverability.

---

## 6️⃣ Testing & Validation

**Scope:**
- Update all tests that reference pake.
- Validate CLI commands execute successfully.
- Ensure Rust build (cargo build and cargo test) passes.
- Validate Node/pnpm build (pnpm run build, pnpm run dev) passes.
- Confirm watermark appears and is minimally intrusive but persistent.
- Re-run tests after each rename layer.

---

## 7️⃣ Workflow & CI/CD Updates

**Files:**
- .github/workflows/*.yml
- action.yml

**Tasks:**
- Rename workflow identifiers to webpg2app.
- Update artifact names to webpg2app.
- Ensure that any CI scripts or GitHub Actions references to the original repository now point to the forked webpg2app.
- Maintain build and release pipeline functionality.

---

## 8️⃣ Optional Professional Recommendations

- Fork under a personal or organization account for long-term maintenance.
- Keep a clean staged commit history (docs → CLI → Rust → Tauri → workflows → tests).
- Validate all changes with continuous integration.
- Document contributors and maintainers for clarity.
- Consider ethical telemetry or auto-update mechanisms for future versions.
- Ensure MIT license compliance.

---

## 9️⃣ Summary of Tasks for AI

1. Identify and categorize all instances of pake and Pake.
2. Rename all occurrences to webpg2app in CLI, Rust, Tauri, docs, tests, workflows, and binaries.
3. Inject permanent, minimal watermark with mwakidenis alternating black and red letters.
4. Restructure all documentation for clarity and SEO.
5. Validate build, CLI, and Tauri functionality after every layer of changes.
6. Set up development environment instructions and CI/CD guidance.
7. Provide clear commit strategy and staged update recommendations.
