# Writing for the web

## Summary

People read on screens by scanning: they look at headings, the start of paragraphs and anything that stands out, and decide quickly whether to read further. Copy for the web therefore puts the conclusion first, uses descriptive headings, short paragraphs, lists for parallel items, plain words and specific numbers. Readability formulas and plain language standards give measurable targets, and a disciplined editing process removes most of what makes copy weak. Clear writing is also accessible writing, which the European Accessibility Act now makes a legal concern for many online shops.

## Prerequisites

[Copywriting fundamentals](copywriting-fundamentals.md).

## Core concepts

### Definition

*Writing for the web* is the practice of writing text for screens so that readers can find, understand and act on what they need with the least effort. It includes structure (order and headings), style (words and sentences), *microcopy* (the short text on buttons, forms and error messages) and editing.

*Analogy.* A web page is read like a road sign at speed, not like a novel in an armchair. The driver glances, picks out the one word that matters (the exit name) and moves on. A sign that hides the exit name in the middle of a sentence causes missed turns. The analogy breaks because a web reader who finds something relevant does slow down and read closely, so a page must work both as a sign and as a text.

### How people read on screens

- **Scanning.** In Jakob Nielsen's 1997 usability tests, 79% of test users always scanned new pages and only 16% read word by word.
- **The F-pattern.** Eye-tracking studies by the Nielsen Norman Group (2006) found that on text-heavy pages many users read across the top, then across a shorter line below, then scan down the left side, forming a rough F. Later work stressed that the pattern appears when pages are poorly formatted, and that good headings and lists change it.
- **Concise, scannable, objective.** In the companion study by Morkes and Nielsen (1997), a sample site rewritten to be concise, scannable and objective measured 124% better usability than the original. The study used one site and one text, so the size of the gain is an illustration, not a law.

### Structure: conclusion first

The *inverted pyramid*, taken from news writing, puts the most important information first and details later. For copy this means: the benefit or the answer in the first sentence, the supporting detail after. A reader who stops after one paragraph should still have the main message.

Practical rules:

- One idea per paragraph, and the idea in the first sentence.
- Headings that describe the content ("Shipping costs and times") rather than tease it ("The fine print").
- Lists for parallel items (features, steps), not for every thought.
- Bold for the few words a scanner must not miss, used sparingly.
- Numbers as digits ("3 days", "15%"), which stand out when scanning.

### Readability

*Readability* is how easy a text is to read and understand. *Readability formulas* estimate it from sentence length and word length:

- The *Flesch Reading Ease* score (Flesch, 1948) is 206.835 − 1.015 × (words per sentence) − 84.6 × (syllables per word). Higher is easier. Scores of 60 to 70 correspond roughly to plain English.
- The *Flesch-Kincaid Grade Level* translates a similar calculation into a US school grade.

Formulas measure only surface features. A text with short words and short sentences can still be unclear or wrong. Use them as a warning signal for long sentences and heavy vocabulary, not as a goal in themselves.

```python
# Python 3.13. Rough Flesch Reading Ease for a short English text.
# The syllable counter is a simple heuristic and makes errors on some words.
import re

def syllables(word: str) -> int:
    word = word.lower()
    groups = re.findall(r"[aeiouy]+", word)
    count = len(groups)
    if word.endswith("e") and count > 1:
        count -= 1  # silent final e
    return max(count, 1)

def reading_ease(text: str) -> float:
    sentences = [s for s in re.split(r"[.!?]+", text) if s.strip()]
    words = re.findall(r"[A-Za-z']+", text)
    syl = sum(syllables(w) for w in words)
    return 206.835 - 1.015 * len(words) / len(sentences) - 84.6 * syl / len(words)

before = ("Our innovative solution facilitates the optimization of hydration "
          "throughout the entirety of the working day.")
after = "Your water stays cold all day. Even at your 4 pm meeting."
print(round(reading_ease(before), 1), round(reading_ease(after), 1))
```

Output:

```text
-5.8 93.6
```

The first sentence scores far below zero because of its long words. The rewritten version scores in the easy range. The heuristic syllable counter makes the exact numbers approximate.

### Plain language

*Plain language* is writing that the intended reader can find, understand and use. It has become a formal standard: ISO 24495-1:2023 sets out principles for plain language in written documents, and the US Plain Writing Act of 2010 requires federal agencies to use it. The principles apply to copy:

- Write for a specific reader.
- Use words the reader uses (see [customer research](customer-research.md)).
- Prefer the active voice and concrete subjects.
- Keep sentences short, on average under about 20 words.
- Explain unavoidable technical terms.

### Microcopy

*Microcopy* is the small text that guides action: button labels, form field hints, error messages, confirmation messages, empty states. It has a large effect because it appears at the moment of action.

- **Buttons** say what happens: "Create account", "Download the template", not "Submit".
- **Error messages** say what went wrong and how to fix it, without blame: "The card number has 15 digits. Please check the last digit."
- **Forms** explain why sensitive information is needed: "We use your phone number only to arrange delivery."

### Editing process

Most good copy is rewritten several times. A practical sequence of editing passes, each with one focus:

1. **Purpose.** Is the reader, the promise and the action clear? Cut anything that does not serve them.
2. **Structure.** Is the conclusion first? Do headings tell the story on their own?
3. **Claims.** Is every claim specific and supported? Remove or prove superlatives.
4. **Sentences.** Split long sentences. Replace passive with active voice where the actor matters.
5. **Words.** Replace jargon and vague words ("solution", "innovative", "seamless") with concrete ones.
6. **Read aloud.** Awkward rhythm and missing words show up when spoken.
7. **Proofread** last, preferably after a break or by someone else.

### Accessibility

Accessible copy can be used by people with disabilities, including people using screen readers, people with cognitive disabilities and people reading in a second language. The Web Content Accessibility Guidelines (WCAG 2.2, W3C, 2023) include requirements that concern text: meaningful link text, descriptive headings and labels, text alternatives for images, and clear error identification. In the EU, the European Accessibility Act (Directive (EU) 2019/882) applies since 28 June 2025 to e-commerce services offered to consumers, with exemptions for microenterprises providing services. Clear writing is therefore partly a legal requirement for many online shops.

## Worked example

A shipping information section before and after editing.

**Before (122 words, one paragraph):**

> At ShopName we are committed to providing an outstanding customer experience, which is why we work with a selection of leading logistics partners in order to ensure that your order can be delivered in a timely and efficient manner. Delivery times may vary depending on a number of factors including, but not limited to, your location and the availability of the products ordered. In most cases orders placed before the daily cut-off will be dispatched on the same working day. Shipping is free for orders above a certain value, while a fee applies to orders below that threshold. For further information please do not hesitate to contact our friendly customer service team, who will be happy to assist you with any questions you may have.

**After (structured, 52 words):**

> **Shipping**
>
> - Order by 2 pm on a working day and we ship the same day.
> - Delivery in Poland: 1 to 2 working days. EU: 3 to 5 working days.
> - Free shipping over 150 PLN. Below that: 14.99 PLN.
>
> Questions? Write to us at shop@example.com. We answer within one working day.

The edited version answers the three questions buyers ask (when, how long, how much) with numbers, can be scanned in seconds and removes self-praise. The figures are invented.

## Trade offs and when to use it

- **Concise versus complete.** Cutting too much removes the detail a careful buyer needs. Put essentials first and details behind a link or in an expandable section.
- **Plain versus expert.** Expert audiences expect precise terms. Plain does not mean simplistic: use the terms your readers use.
- **Readability scores versus meaning.** Optimizing a score can produce choppy text. Use scores as a check, then read the text as a reader would.
- **Brand voice versus clarity.** A playful voice is fine if the key information stays clear.

## Common mistakes

- **Burying the answer.** Fix: first sentence answers the question.
- **Clever headings.** Fix: descriptive headings that work on their own.
- **Vague buttons.** Fix: verbs that say what happens.
- **Walls of text on mobile.** Fix: short paragraphs and lists.
- **Editing everything in one pass.** Fix: one focus per pass.

## Practice

1. What share of users scanned pages in Nielsen's 1997 tests, and what are the limits of the 124% figure?
2. Calculate the Flesch Reading Ease of one of your own paragraphs with the script above, then rewrite the paragraph and compare.
3. Rewrite three button labels on a site you use so they say what happens.
4. Which EU law makes accessible e-commerce copy a legal concern since June 2025?

## Further reading

- Nielsen, J. (1997). How users read on the web. Nielsen Norman Group. [nngroup.com](https://www.nngroup.com/articles/how-users-read-on-the-web/). Scanning behavior.
- Nielsen, J. (2006). F-shaped pattern for reading web content. Nielsen Norman Group. [nngroup.com](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content-discovered/). Eye-tracking findings.
- Flesch, R. (1948). A new readability yardstick. *Journal of Applied Psychology*, 32(3), 221-233. [doi:10.1037/h0057532](https://doi.org/10.1037/h0057532). The Reading Ease formula.
- ISO 24495-1:2023. Plain language, Part 1: Governing principles and guidelines. [iso.org](https://www.iso.org/standard/78907.html). The international plain language standard.
- W3C (2023). Web Content Accessibility Guidelines (WCAG) 2.2. [w3.org](https://www.w3.org/TR/WCAG22/). Accessibility requirements for web content.
- Directive (EU) 2019/882 on the accessibility requirements for products and services (European Accessibility Act). [EUR-Lex](https://eur-lex.europa.eu/eli/dir/2019/882/oj). Accessibility of e-commerce services in the EU.

TODO: Verify the URLs of the 2006 F-pattern article and the ISO 24495-1 catalog page, and the exact scope of the microenterprise exemption in the European Accessibility Act.
