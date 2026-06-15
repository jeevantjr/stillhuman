# The Day My AI Assistant Disagreed With Itself

*Same data. Same sources. Same instructions. Two different answers. Neither was wrong.*

---

A few weeks ago I was testing an AI tool I had built for cancer registry coding work.

I ran the same nine records through it twice. Same notebook. Same reference materials. Same prompt. The only difference was time.

First run: all nine records classified as **VALID**.

Second run: eight VALID, one flagged as **RARE BUT VALID** — with a clinical note I had not asked for, recommending that staff verify the case before finalising the code.

I stopped and looked at this for a while.

---

## What I Had Built

Cancer registries use a classification system called ICD-O — the International Classification of Diseases for Oncology — to code tumour diagnoses. The coding requires matching morphology (what the cancer looks like) with topography (where it is in the body). Some combinations are common. Some are rare but valid. Some are errors.

I built an AI assistant to help with this — not to replace the registrar, but to act as an intelligent reference tool. Rather than letting the model generate answers from its general training, I grounded it in a curated set of ICD-O reference materials and instructed it to answer *only* from those sources.

I thought this addressed the main risk: hallucination. The model could not invent things. It had to work from fixed, authoritative sources.

![ICD-O-3.2 Coding Reference Notebook in Google NotebookLM](https://drjeevaraj.com/images/imagesai-notebook-setup.png.jpeg)

*The notebook-based AI system, built with curated ICD-O-3.2 reference sources.*

I felt reasonably confident. The workflow was controlled. The sources were fixed.

Then the system disagreed with itself.

---

## The Two Runs

The record in question was a squamous cell carcinoma associated with the parotid gland — an uncommon but permissible combination in ICD-O.

**First run:**

![First run — all 9 VALID](https://drjeevaraj.com/images/imagesai-run1-valid.png.jpeg)

All nine records VALID. No flags. No manual review recommendations.

**Second run — same data, same everything:**

![Second run — one flagged RARE BUT VALID](https://drjeevaraj.com/images/imagesai-run2-rare.png.jpeg)

Eight VALID. One RARE BUT VALID. The system now noted that squamous cell carcinoma is an uncommon primary malignancy in the parotid gland, and recommended verifying whether the case might represent a metastasis rather than a primary tumour.

Same reference material. Two different conclusions.

---

## Neither Was Wrong

My first instinct was to find the mistake. The more carefully I looked, the more I realised there was no mistake in the conventional sense.

The ICD-O combination was permissible — so VALID was a defensible classification. And the clinical note in the second run was also accurate — squamous cell carcinoma *is* uncommon in the parotid, and the recommendation to verify was not unreasonable. It was arguably good practice.

Both outputs were grounded in the same source material. Both could be justified.

> **The issue was not hallucination. The issue was interpretation.**

The model had not fabricated anything. It had simply weighed the clinical context differently — evaluated the significance of rarity differently — in the second session than in the first.

This is a distinction that matters enormously in healthcare.

---

## What This Taught Me

Most discussions about AI risk in healthcare focus on hallucination — the risk that a model generates plausible but incorrect information. That is a real risk, and one worth designing against.

But this experience introduced me to a second category of risk that receives much less attention: **interpretive variability**.

Traditional software behaves deterministically. Same input, same output, every time. Large language models do not always work this way — even when grounded in fixed sources, even when given precise instructions. They reason. And reasoning, unlike retrieval, can arrive at different conclusions from the same starting point.

In a general knowledge context, this kind of variability is often acceptable — even desirable. In a cancer registry, a clinical coding department, or a public health reporting system, it is operationally significant.

A record that is VALID on Monday and RARE BUT VALID on Thursday, with no change in data or instructions, is a governance problem.

---

## Why Human-in-the-Loop Is Not a Temporary Fix

I want to be direct about something that I think gets lost in discussions about AI progress.

The phrase "human-in-the-loop" is often presented as a transitional arrangement — a precaution we need until AI systems become accurate enough to act autonomously. I do not believe this framing is correct, at least not in healthcare.

Human oversight in healthcare is not a safety net waiting to be removed. It is part of the design. Healthcare decisions carry professional, legal, and ethical accountability that cannot be delegated to an algorithm. Even a perfectly accurate system would still require human accountability for the decisions made using its outputs.

The goal of clinical AI is not to remove people from the loop. It is to help people inside the loop make better, faster, better-informed decisions.

---

## What I Would Tell Anyone Building Similar Tools

From this experience, five things I now think are essential:

**Source grounding is necessary but not sufficient.** It addresses hallucination. It does not address interpretive variability. These are different problems requiring different governance approaches.

**Prompt engineering reduces risk — it does not eliminate variability.** Even well-designed instructions cannot guarantee identical outputs from a probabilistic system.

**Two defensible outputs are still a governance problem.** The question is not only whether each output is correct in isolation, but whether the system behaves consistently enough to be relied upon in an operational setting.

**Human review is not a workaround.** It is the layer that converts AI output into accountable professional action. It should be designed in from the beginning, not added apologetically at the end.

**AI governance must account for consistency, not only accuracy.** A system that is accurate on average can still produce clinically meaningful variation at the individual case level.

---

## A Final Thought

The tool I built worked. It reduced the time required to validate coding combinations, flagged unusual cases that might otherwise have been missed, and helped surface clinical context that supported better decision-making.

And it also reminded me, clearly, that the most effective clinical AI model is not AI alone.

It is AI, combined with human expertise, structured review, and clear accountability — operating together as a system designed to produce consistent, trustworthy outputs in environments where the margin for unreviewed error is narrow.

*Technology can help us work faster and more efficiently. But trust in healthcare depends on something that remains human: professional judgement, accountability, and responsibility. That is not a weakness of AI. It is a reminder of how AI and humans are designed to work together.*

---

**Dr. T. Jeevaraj** · MBBS · MCGP · MSc Biomedical Informatics · MD Trainee, Health Informatics, PGIM, University of Colombo.

I write here about what AI does to ordinary human life — not the technology itself, but what it quietly changes in the people who use it.

My first English book, *Are You Still Human? (2026)*, is available on [Amazon Kindle](https://www.amazon.com/dp/B0H333G41P) (including Kindle Unlimited).

[drjeevaraj.com](https://drjeevaraj.com) · Read the full illustrated version with screenshots: [drjeevaraj.com/ai-consistency-nccp.html](https://drjeevaraj.com/ai-consistency-nccp.html)

---

*If someone forwarded this to you and you found it useful, you can subscribe here to receive future articles directly.*
