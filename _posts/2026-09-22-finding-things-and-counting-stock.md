---
layout: post
title: "Improved way to take stock, error aware search"
date: 2026-09-22
category: Shuwaki Worxpace feature update
image_path: /assets/images/stock-page.png
---


Two changes in Worxpace 2.7.5 that you need to know about.

Two parts of Worxpace have been rebuilt. Neither is a new button to learn. One makes a thing you do
two hundred times a day more human nature-tolerant, and the other makes it right, finally, to stop
counting stock with pen and paper

---

## About searching

### It finds what you meant

The old search already does a number of good things. It looks in multiple attributes of the items
(name, description, group, barcode, price, and manufacturer, MA holder, constituents for drugs) and
takes in multiple words. “amox 500” returns amoxicillin 500mg

Now:

- **A typo still finds it.** "amoxicilin" finds *Amoxicillin*. Worth having when you are typing
  quickly with somebody waiting.
- **The best match comes first**, rather than whatever happened to be first alphabetically. Coupled
  with popularity ranking (where ‘paracetamol’ returns ‘tab paracetamol’ before ‘IV paracetamol
  100ml’), this looks almost like reading your mind

The same search now runs in the cart, on the products page, on services, and in a stock take. One
search box that behaves the same way everywhere.

---

## Counting stock

### The problem

Stock counting is usually multiple people with a shelf each. Worxpace only ever kept one figure per
item, and whoever saved last won.

So if you counted the paracetamol and found 40, and your colleague counted the same shelf an hour
later and found 37, the count said 37. Your 40 was gone. Nothing told either of you that two
different people had counted the same thing and disagreed — which is exactly the moment you most
want to know.

That is a bad way to lose information. The disagreement is the *useful* part: it usually means one
of you missed a box, or there is stock somewhere you did not expect.

### What happens now

**Both figures are kept.** The first count goes onto the sheet. A second, different count from
somebody else is held to one side, and the count shows you how many are waiting.

**Somebody decides.** A new screen, **Resolve issues**, puts the two figures side by side — what
each person counted, who counted it, and when — and offers four choices:

| | |
| --- | --- |
| **Keep the first count** | The second person was looking at the wrong shelf. |
| **Take the second count** | The first person missed something. |
| **Add both together** | You each counted a different box of the same item. |
| **Enter a different number** | You went and looked, and it is neither. |

Nothing is decided for you and nothing is thrown away quietly.

**Agreement is shown as agreement.** If two people report the same number, that appears as *Same
figure* rather than a dispute — confirm it and move on. Worxpace cannot tell "we agree" from "we
both counted the same shelf twice", so it asks rather than guesses.

### A count now has a state

Three of them:

- **In progress** — people are still counting.
- **Completed** — counting has finished and the figures have settled.
- **Applied** — the difference has been posted to your stock.

A count can only be applied **once**, even if two people press the button at the same moment, and an
applied count becomes read-only: it is the record of what was posted to your stock, so it should not
change afterwards. Reopening a completed count is an administrator's decision.

You also cannot finish a count while figures are still waiting to be reconciled. That is deliberate.
A count is not finished while two people still disagree about what is on the shelf.

### Smaller things

- **Half a box is a real quantity.** Counts take decimals now, instead of rounding to whole numbers.
- **Expiry dates are recorded with the count**, not copied from the product record — because two
  people finding the same item with different expiry dates is worth knowing about.
- **A count belongs to one location**, so you cannot accidentally count another branch's stock into
  it.
- **Stock taking now works in the browser** as well as on the desktop, with the same rules.

---

*Worxpace 2.7.5. Talk to us before upgrading if you run more than one location.*
