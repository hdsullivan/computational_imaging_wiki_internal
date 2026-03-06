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
A paper belongs here if it falls into either of these categories:

**Established impact** — work the community broadly recognizes as essential:
- Introduced a method, framework, or idea that the subfield is built on
- Widely cited and adopted as a standard reference or benchmark
- Fundamentally shifted how researchers approach a problem

**Emerging work** — recent papers not yet widely adopted, but with a clear case for exceptional significance:
- Represents a genuine step-change in methodology or results, not an incremental improvement
- Comes with a strong contributor explanation of *why* it clears the bar (required in the PR)

The gut-check question for both: *does this change how people think about the problem, or is it likely to?* Incremental improvements, workshop papers, and routine applications of existing methods are not a good fit regardless of novelty.

### Datasets
Datasets should be well-documented and either widely used as a benchmark already, or newly released with a clear case for why they will become one — strong coverage, a credible source, and an obvious gap they fill. Niche or single-use datasets without broader applicability are not a good fit.

### Code & Software
Code should be well-maintained, publicly documented, and either already in broad use or a high-quality reference implementation of an important method. Emerging tools from active research groups are welcome if they are clearly documented and filling a real gap. Personal research code without documentation or community adoption is not a good fit.

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

If your resource doesn't fit any existing subfield, you can propose a new one — but new subfields require an area lead to be active from the start. A wiki page with no one tending it quickly goes stale.

To propose a new subfield:

1. Open a [GitHub Discussion](../../discussions) with the label `new-subfield`.
2. Include a one-paragraph motivation: what is this subfield and why does it belong in a computational imaging wiki?
3. List at least **3 seed resources** you would add immediately, each clearly meeting the quality bar above.
4. **Name an area lead** — either yourself or someone who has agreed to take on the role. New subfields will not be approved without a committed area lead.
5. Once a maintainer approves, create a new file under `docs/` using `docs/_template.md` as your starting point.

Being an area lead is a light commitment: reviewing the occasional PR in your subfield and keeping an eye on link quality over time. It does not require ongoing curation or content creation.

---

## Moderation

Each subfield has one or two **area leads** responsible for reviewing PRs in that domain. Reviewers will check that submitted papers meet the quality bar — incremental or unestablished work will be declined with a brief explanation.

If your PR sits unreviewed for more than a week, feel free to tag a maintainer in the PR comments. To become an area lead, open a GitHub Discussion expressing interest.
