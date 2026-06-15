# The Day My AI Assistant Disagreed With Itself

## Reflections from building an ICD-O coding support assistant for cancer registry work — and what happened when the same system gave two different answers to the same question.

---

I have spent much of my professional life working at the intersection of healthcare, information systems, and data quality. In recent years, like many others in health informatics, I have become increasingly interested in how artificial intelligence can support routine but important tasks — and where it still requires careful human guidance.

One area where I saw genuine potential was cancer registry coding. Cancer registries depend heavily on accurate classification using international standards such as the International Classification of Diseases for Oncology (ICD-O). Even experienced staff occasionally encounter uncommon combinations of topography and morphology codes that require checking against reference materials. I wondered whether AI could help streamline that process — acting as an intelligent reference assistant rather than replacing the professional judgement behind it.

So I decided to build one.

---

![ICD-O-3.2 Coding Reference Notebook built in Google NotebookLM](https://drjeevaraj.com/images/imagesai-notebook-setup.png.jpeg)

*Figure 1: The ICD-O-3.2 Coding Reference Notebook, built using a notebook-based AI system. Sources were carefully curated to include only authoritative ICD-O references. The system was instructed to answer only from these sources.*

---

Rather than allowing a language model to generate answers freely from its general training, I took a more controlled approach. I created a notebook-based system and supplied it with carefully selected ICD-O reference resources. The prompt was designed to instruct the model to use *only* those approved sources when validating codes or generating coding suggestions.

From a technical perspective, I felt reasonably confident. The sources were fixed. The instructions were fixed. The workflow was fixed. In my mind, I had already addressed one of the most commonly discussed risks in AI systems: hallucination. The model could not generate answers from nothing — it was anchored to a curated set of authoritative resources.

Then something unexpected happened.

---

## A Small Difference That Caught My Attention

While testing the system, I entered a small set of cancer registry records for validation. One of the records involved a squamous cell carcinoma morphology code associated with the parotid gland — a combination that is permissible within ICD-O but uncommon in clinical practice.

The system reviewed the records and produced a validation report. Everything appeared normal. The record in question was classified as **VALID**. There were no flags, no warnings, no recommendations for review.

![First validation run — all 9 records VALID](https://drjeevaraj.com/images/imagesai-run1-valid.png.jpeg)

*Figure 2: First validation run. All nine records, including the squamous cell carcinoma / parotid gland combination, were classified as VALID. No records were flagged for manual review.*

Later, I repeated the same exercise. The same data. The same notebook. The same reference materials. The same instructions. The only difference was time.

This time, however, the output was slightly different. The same record was now classified as **RARE BUT VALID**. The system's explanation stated that squamous cell carcinoma is uncommon as a primary malignancy of the parotid gland, and recommended that staff verify whether the case represented a metastasis rather than a primary tumour before finalising the code.

![Second validation run — one record flagged as RARE BUT VALID](https://drjeevaraj.com/images/imagesai-run2-rare.png.jpeg)

*Figure 3: Second validation run, identical data. VALID: 8 · RARE BUT VALID: 1. Serial No. 3 was flagged with a clinical note recommending manual verification.*

I paused. The difference was subtle, but it was operationally significant. The AI had not simply repeated its previous conclusion. In the second run, it had applied an additional layer of clinical interpretation — one that was entirely absent in the first.

---

## Was One Answer Wrong?

My first instinct was to determine which answer was correct and treat the other as an error. The more carefully I examined both outputs, however, the more I realised that neither answer was necessarily wrong.

The ICD-O coding combination itself was permissible. From a strict coding perspective, the record could reasonably be considered valid. At the same time, the second output introduced useful and clinically accurate context. Squamous cell carcinoma is indeed less common as a primary parotid malignancy compared with mucoepidermoid carcinoma or acinic cell carcinoma. Recommending verification was not an unreasonable step — it was arguably good practice.

Both conclusions could be justified using the same source material.

> **The issue was not hallucination. The issue was interpretation.** The AI did not fabricate information. Both outputs were grounded in the same reference material. The difference arose from how the model evaluated emphasis, clinical context, and the significance of rarity — not from a failure to follow its instructions.

---

## An Important Lesson About AI

This experience revealed something that is sometimes underappreciated in discussions about artificial intelligence deployment in healthcare.

Many people assume that if an AI system receives the same question, the same source material, and the same instructions, it should always produce exactly the same answer. Traditional rule-based software behaves that way. Large language models do not always behave that way — and this distinction matters enormously in clinical and registry environments.

> Even when grounded in fixed sources, language models may evaluate emphasis, clinical context, or the weight of uncertainty differently from one session to another. That is not a system failure. That is the nature of reasoning under probabilistic conditions.

The challenge for healthcare is that clinical and administrative workflows often depend on consistency. A variation that might be considered an acceptable nuance in a general knowledge application may carry meaningful operational consequences in a cancer registry, a clinical coding department, or a public health reporting system.

---

## Why This Changed My Thinking

Before building this tool, I thought primarily about AI risk in terms of hallucination — the risk of a model generating plausible but incorrect information from its general training data. That was the risk I had designed against, and I had largely addressed it through source grounding.

After this experience, I began thinking more comprehensively about **consistency, governance, and accountability**. Hallucination is one category of risk. Interpretive variability is another — subtler, harder to detect, and in some ways more difficult to manage precisely because both outputs appear defensible.

This observation reinforced something I had believed in principle but now understood from practice: artificial intelligence should augment healthcare professionals, not replace them. The most effective clinical AI model is not AI alone. It is AI combined with human expertise, structured review, and clear accountability.

An experienced cancer registrar can recognise when a result deserves closer examination. An AI assistant can accelerate the search for relevant information, flag unusual patterns, and reduce the burden of routine documentation work. Together, they are more effective than either working independently.

---

## Why Human-in-the-Loop Still Matters

The phrase "human-in-the-loop" is sometimes presented as if it were a transitional measure — a bridge that will become unnecessary as AI systems improve in accuracy and reliability. I hold a different view.

In healthcare, human involvement is not merely a safety mechanism. It is a core feature of the system design. Healthcare decisions carry ethical, legal, and professional responsibilities that cannot be delegated to an algorithm — regardless of how accurate that algorithm becomes. Even highly reliable AI systems operate within a framework of human accountability.

When we design AI tools for clinical and public health environments, the objective should not be to remove people from the process. The objective should be to help people make better, faster, and better-informed decisions.

---

## What I Took Away

Building this ICD-O coding support assistant was a genuinely valuable experience. The system worked. It successfully used reference materials to assist with coding validation, reduced the time required to manually search through documentation, and highlighted unusual cases that might otherwise have been missed on a first pass.

But it also demonstrated an important reality that I believe every health informatician, clinical AI developer, and healthcare administrator should understand:

**1. Source grounding reduces hallucination — but does not eliminate interpretive variability.** These are two distinct risks requiring different mitigation strategies.

**2. Prompt engineering reduces risk** — but language model outputs under probabilistic conditions will not always be identical even when instructions are well-designed.

**3. Two outputs can both be justifiable** from the same source material while differing in clinical implication. This is not a flaw — it is a reminder that reasoning is not the same as retrieval.

**4. Human oversight is not optional** in high-stakes healthcare environments. It is the structural layer that converts AI output into accountable professional action.

**5. AI governance must account for consistency, not only accuracy.** A system can be accurate on average and still produce clinically meaningful variation in individual outputs.

For me, this was not a reason to distrust AI. It was a reason to understand it better — and to design the workflows around it more carefully.

---

*Technology can help us work faster. It can help us process information more efficiently. It can help us identify patterns that deserve attention. But trust in healthcare still depends on something fundamentally human: professional judgement, accountability, and responsibility. That is not a weakness of AI. It is a reminder of how AI and humans are designed to work together.*

---

**Dr. T. Jeevaraj** is a medical doctor and health informatics professional (MBBS, MCGP, MSc Biomedical Informatics), currently an MD Trainee in Health Informatics at PGIM, University of Colombo, Sri Lanka. He is the author of *[Are You Still Human? (2026)](https://www.amazon.com/dp/B0H333G41P)*.

Website: [drjeevaraj.com](https://drjeevaraj.com) · X: [@drjeevaraj](https://x.com/drjeevaraj)

---

*Tags: AI in Healthcare · Health Informatics · Cancer Registry · Responsible AI · Human in the Loop · ICD-O · Clinical Coding · Digital Health*
