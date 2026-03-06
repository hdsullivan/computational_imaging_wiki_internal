---
title: [Subfield Name]
nav_order: 99
has_children: true
---

# [Subfield Name]

{: .note }
> 📋 **Using this template:** Copy this file to `docs/your-subfield-name.md` and create a `docs/your-subfield-name/` folder for child pages. Update `title` and `nav_order` in the front matter, and replace all placeholder text.

[2–3 sentences describing this subfield. What is the core problem it addresses? What makes it distinct within computational imaging?]

Browse papers by sub-topic using the sidebar, or jump directly to:
[Sub-topic A](your-subfield-name/sub-topic-a) · [Sub-topic B](your-subfield-name/sub-topic-b)

---

## 🗄️ Datasets

| Title | Link | Description |
|-------|------|-------------|
| Example Dataset | [Link](https://example.com) | One sentence describing the dataset and why it is a standard benchmark. |

---

## 💻 Code & Software

| Title | Link | Description |
|-------|------|-------------|
| Example Repo | [Link](https://github.com/org/repo) | One sentence describing what the software does and why it is widely used. |

---

{: .highlight }
> 💡 **Want to add something?** Papers should be seminal or widely recognized as important by the community. Datasets and code should be in broad use. [Read the Contribution Guide](../contributing/) before submitting.

---

## Child Page Template

For each sub-topic, create a file at `docs/your-subfield-name/sub-topic-name.md` with this front matter:

```yaml
---
title: [Sub-topic Name]
parent: [Subfield Name]   # must match the title above exactly
nav_order: 1
---
```
