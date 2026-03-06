---
title: Contributing
permalink: /contributing/
nav_order: 9
---

# Contributing to the Computational Imaging Wiki

This wiki is intentionally selective. The goal is a resource researchers can trust — a list of papers that genuinely shaped the field, not an exhaustive archive. Before contributing, please read the standards below carefully.

---

## What Belongs Here

### Papers
Papers should meet at least one of these criteria:
- **Foundational** — introduced a method, framework, or idea that the subfield is built on
- **Widely cited and adopted** — work the community broadly recognizes as a standard reference or benchmark
- **Game-changing** — a recent result that has clearly shifted how researchers approach a problem

If you're unsure whether a paper clears the bar, ask yourself: *would a researcher new to this subfield need to read this to understand the landscape?* If the honest answer is no, it's probably not ready for this wiki.

Papers that are **not** a good fit: incremental improvements, workshop papers, preprints without significant community uptake, or work whose long-term impact hasn't been established yet.

### Datasets
Datasets should be widely used as benchmarks in the community — ones that appear repeatedly in comparisons across papers. Niche or single-paper datasets are not a good fit unless they've become a standard.

### Code & Software
Code should be well-maintained, publicly accessible, and in broad use. Reference implementations of landmark methods are ideal. Personal research code with no documentation or community adoption is not a good fit.

---

## How to Contribute (Step by Step)

1. **Fork** this repository to your own GitHub account.
2. **Find the right file** under `docs/` for the subfield your resource belongs to. Not sure? Pick the closest match or propose a new subfield (see below).
3. **Add your entry** to the correct section (Papers, Datasets, or Code) using the table format below.
4. **Open a Pull Request** using the PR template — fill in every field, including a clear explanation of why this resource meets the quality bar.
5. **An area lead reviews** your PR and merges if it meets the criteria above.

---

## Table Format

Please copy the format below exactly. Entries that don't follow it will be asked to revise before merging.

**Papers:**

```markdown
| Title | Link | Year | Description |
|-------|------|------|-------------|
| Your Paper Title | [Link](https://arxiv.org/abs/xxxx.xxxxx) | 2024 | One sentence on what this paper introduced and why it matters. |
```

**Datasets:**

```markdown
| Title | Link | Description |
|-------|------|-------------|
| Your Dataset Name | [Link](https://example.com) | One sentence describing the dataset and why it's a standard benchmark. |
```

**Code & Software:**

```markdown
| Title | Link | Description |
|-------|------|-------------|
| Your Repo Name | [Link](https://github.com/org/repo) | One sentence describing what the software does and why it's widely used. |
```

---

## Writing Good Descriptions

Descriptions should explain **why** a resource matters, not just what it is. Compare:

- ❌ *"A paper about image reconstruction using deep learning."*
- ✅ *"Introduced the U-Net architecture with skip connections, which became the dominant model for biomedical image segmentation."*

Assume the reader is a researcher in a neighboring subfield who needs to quickly understand the significance of the work.

---

## Proposing a New Subfield

If your resource doesn't fit any existing subfield:

1. Open a [GitHub Discussion](../../discussions) with the label `new-subfield`.
2. Include a one-paragraph motivation: what is this subfield and why does it belong in a computational imaging wiki?
3. List at least **3 seed resources** you would add immediately, each clearly meeting the quality bar above.
4. Once a maintainer approves, create a new file under `docs/` using `docs/_template.md` as your starting point.

---

## Moderation

Each subfield has one or two **area leads** responsible for reviewing PRs in that domain. Reviewers will check that submitted papers meet the quality bar — incremental or unestablished work will be declined with a brief explanation.

If your PR sits unreviewed for more than a week, feel free to tag a maintainer in the PR comments. To become an area lead, open a GitHub Discussion expressing interest.
