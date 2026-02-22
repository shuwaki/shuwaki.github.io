---
layout: post
title: "Pharmacy Software Design Manifesto: A boundary-first philosophy for building systems that respect pharmacy practice"
date: 2026-02-22
category: Sofware Development
image_path: /assets/images/design-manifesto-image.jpg
---
Pharmacy software does not practice pharmacy, Pharmacists do.

Software exists to **support judgment, preserve safety, and reduce
cognitive load** --- not to replace professional responsibility. This
manifesto defines where software should be strong, where it should be
silent, and where it must step aside.

------------------------------------------------------------------------

## 1. Judgment Belongs to the Pharmacist

**Principle:** Software may inform decisions, but must never own them.

-   Software can calculate, warn, and compare.
-   Pharmacists decide, override, and take responsibility.

**Design implication:** - Every critical decision must be explicitly
human-confirmed. - Overrides must be possible, visible, and accountable.

------------------------------------------------------------------------

## 2. Safety Through Guardrails, Not Walls

**Principle:** Safety comes from guidance, not prohibition.

-   Hard blocks create unsafe workarounds.
-   Soft warnings preserve workflow while highlighting risk.

**Design implication:** - Prefer warnings over locks. - If a block
exists, it must be legally unavoidable.

------------------------------------------------------------------------

## 3. Relevance Over Correctness

**Principle:** The most relevant information is more valuable than the
most complete information.

-   Pharmacists work under time pressure.
-   Top-ranked results matter more than exhaustive lists.

**Design implication:** - Rank results by intent, not string match. -
Bias toward recent, common, and equivalent options.

------------------------------------------------------------------------

## 4. Forgiveness Is a Feature

**Principle:** Input errors are normal; system rigidity is not.

-   Misspellings, abbreviations, and partial memory are expected.

**Design implication:** - Searches must tolerate ambiguity. - The system
should try to help before it rejects.

------------------------------------------------------------------------

## 5. Exceptions Are the Rule

**Principle:** Real pharmacy practice lives in edge cases.

-   Perfect data is rare.
-   Context always matters.

**Design implication:** - Make exceptions easy to perform. - Make them
impossible to hide.

------------------------------------------------------------------------

## 6. Accountability Must Be Explicit

**Principle:** If something goes wrong, responsibility must be
traceable.

-   Software logs.
-   Humans are accountable.

**Design implication:** - Every override, substitution, and refusal must
have identity and timestamp. - Never attribute decisions to "the
system".

------------------------------------------------------------------------

## 7. Silence Is Better Than Noise

**Principle:** Alert fatigue is a patient safety issue.

-   Too many warnings equal no warnings.

**Design implication:** - Alerts must be tiered, suppressible, and
explainable. - Pharmacists should control alert behavior.

------------------------------------------------------------------------

## 8. UX Is Ethics

**Principle:** Interface design shapes professional behavior.

-   Click counts matter.
-   Default options influence outcomes.

**Design implication:** - Design defaults carefully. - Avoid layouts
that rush irreversible actions.

------------------------------------------------------------------------

## 9. Local Practice Beats Global Assumptions

**Principle:** Pharmacy is culturally and legally local.

-   What is acceptable in one place may not be in another.

**Design implication:** - Make rules configurable. - Avoid hardcoding
moral or cultural norms.

------------------------------------------------------------------------

## 10. Explain Before You Enforce

**Principle:** A warning without explanation is noise.

**Design implication:** - Every alert should answer: *Why am I seeing
this?* - Provide context, not just color.

------------------------------------------------------------------------

## 11. Software Must Know When to Stop

**Principle:** Some decisions must remain human by design.

If a decision: - Carries ethical weight - Risks professional license -
Depends on unstructured context

Then software must **step aside**.

------------------------------------------------------------------------

## The Red Line

A pharmacy system has failed if it: - Removes professional discretion -
Obscures accountability - Forces unsafe workarounds - Replaces judgment
with automation

------------------------------------------------------------------------

## Closing Statement

Good pharmacy software is invisible when judgment is needed, and
powerful when memory, consistency, and speed are required.

**The goal is not automation. The goal is trust.**
