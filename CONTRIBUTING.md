# Contributing to the Computational Imaging Wiki

Thank you for helping grow this resource! Contributions from the broader research community are what make this wiki useful. This guide explains exactly what belongs here and how to add it.

---

## What Belongs Here

This wiki collects links to:

- **Papers** — published journal/conference papers or preprints (arXiv links are fine) that are relevant to a computational imaging subfield. Both foundational classics and strong recent work are welcome.
- **Datasets** — benchmark datasets or experimental data collections used for training, evaluation, or comparison in the community.
- **Code & Software** — open-source implementations, toolkits, or libraries. The code should be reasonably documented and publicly accessible.

**Acceptance criteria:** A contribution is accepted if it is (1) a real, working link, (2) genuinely relevant to the listed subfield, and (3) accurately described. This is not a curated "best of" list — relevance and accuracy are the bar, not subjective quality judgments.

---

## How to Contribute (Step by Step)

1. **Fork** this repository to your own GitHub account.
2. **Find the right file** under `docs/` for the subfield your resource belongs to. Not sure? Pick the closest match or propose a new subfield (see below).
3. **Add your entry** to the correct section (Papers, Datasets, or Code) using the table format below. Add new rows at the bottom of the table.
4. **Open a Pull Request** back to this repo's `main` branch. Use the PR template — fill in every field.
5. **An area lead reviews** your PR, usually within a few days, and merges if the entry is accurate and relevant.

---

## Table Format

Please copy the format below exactly. Entries that don't follow it will be asked to revise before merging.

**Papers:**

```markdown
| Title | Link | Year | Description |
|-------|------|------|-------------|
| Your Paper Title | [Link](https://arxiv.org/abs/xxxx.xxxxx) | 2024 | One sentence describing what this paper does or why it matters. |
```

**Datasets:**

```markdown
| Title | Link | Description |
|-------|------|-------------|
| Your Dataset Name | [Link](https://example.com) | One sentence describing the dataset contents and typical use case. |
```

**Code & Software:**

```markdown
| Title | Link | Description |
|-------|------|-------------|
| Your Repo Name | [Link](https://github.com/org/repo) | One sentence describing what the software does. |
```

---

## Proposing a New Subfield

If your resource doesn't fit any existing subfield:

1. Open a [GitHub Discussion](../../discussions) with the label `new-subfield`.
2. Include a one-paragraph motivation: what is this subfield and why does it belong in a computational imaging wiki?
3. List at least **3 seed resources** you would add immediately.
4. Once a maintainer approves, create a new file under `docs/` using `docs/_template.md` as your starting point.

---

## Entry Quality Tips

- **Links:** Always verify the link works before submitting. The automated link checker will flag broken links, but it's faster if you check first.
- **Descriptions:** Write in plain language. Assume the reader is a researcher in a neighboring subfield, not the specific paper's area. One clear sentence beats a jargon-heavy paragraph.
- **Duplicates:** Search the page before adding — if a slightly different version of the link already exists (e.g., arXiv vs. published version), add a note in your PR rather than creating a duplicate entry.
- **Self-promotion:** Adding your own papers, datasets, or code is welcome and encouraged, as long as the work is genuinely relevant.

---

## Moderation

Each subfield has one or two **area leads** responsible for reviewing PRs in that domain. If your PR sits unreviewed for more than a week, feel free to tag a maintainer in the PR comments.

To become an area lead for a subfield, open a GitHub Discussion expressing interest. We're always happy to bring in more help.
