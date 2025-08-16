---
title: "Expected Value with Tables, Binomials, and Areas"
date: 2024-12-18
draft: false
description: "Evaluating some bets using the concept of expected value."
tags: ["math", "counting","statistics", "probability"]
---

{{< katex >}}

## What Is Expected Value?

Expected value (EV) tells you, on average, what to expect in a probabilistic setting — like gambling, games, or life.

> **Definition**: Expected value is the weighted average of all outcomes, where each outcome is multiplied by its probability.

For a basic example:

- Heads: earn \( \$5 \)
- Tails: lose \( \$10 \)
- Both have \( \frac{1}{2} \) probability

\[
\text{EV} = \frac{1}{2} \cdot 5 + \frac{1}{2} \cdot (-10) = -2.5
\]

So you lose \$2.50 per flip on average: not a fair game.

---

## Expected Value in the Lottery

Let’s say you analyze the Florida Lottery with outcomes and probabilities. If the weighted sum of your winnings is:

\[
\text{Total EV} = 68
\]

You spent \$2 on the ticket, so your **net expected value** is:

\[
68 - 2 = 66
\]

But suppose the real math gives:

\[
\text{EV} = -1.33
\]

This means you’re losing money in the long run. Even with huge jackpots, the odds are against you.

---

## Word Rearrangement (Counting Methods)

Say you’re arranging letters:

- For the word `ADRI`: All letters are unique. Total permutations:

\[
4! = 24
\]

- For the word `ADRIAN`: Repeated letters must be adjusted:

\[
\frac{6!}{2!} = 360
\]

- Lastly, for the word `SKASKA`: Repeated letters must be adjusted again:

\[
\frac{6!}{2! \cdot 2! \cdot 2!} = 90
\]

---

## True/False Chemistry Test

You take a 10-question true/false test randomly. What’s the chance of scoring exactly 7 correct?

This is a binomial probability problem:

\[
P = \frac{10!}{7! \cdot 3!} \cdot \left( \frac{1}{2} \right)^{10} = \frac{120}{1024} \approx 11.7\%
\]

---

## Area-Based Probability

You shoot a basketball at random on a square backboard of area \( 10 \times 10 = 100 \). The hoop is a circle of radius 3:

\[
\text{Success Area} = \pi \cdot 3^2 = 9\pi \approx 28.27
\]
\[
P(\text{make}) = \frac{9\pi}{100} \approx 0.28
\]

---

## Bet 1: Million-Dollar Target

You pay \$10,000 to shoot a random point at a 25×30 rectangle containing a small diamond-shaped region (formed by joining midpoints of a 2×3 rectangle). Only 2 of 8 internal triangles are shaded:

\[
\text{Success Area} = \frac{1}{4} \cdot 6 = 1.5
\]
\[
\text{Total Area} = 25 \cdot 30 = 750
\]
\[
\text{EV} = \frac{1.5}{750} \cdot 1{,}000{,}000 - 10{,}000 = -\$8{,}000
\]

**Don’t take this bet.**

---

## Bet 2: Deck of Cards

- Draw a card.
- Win \$35,000 if it’s a face card or ace (total of 16 cards).
- Pay \$10,000 to play.

\[
\text{P(win)} = \frac{16}{52},\quad \text{EV} = \frac{16}{52} \cdot 35{,}000 - 10{,}000 = -\$2{,}230.77
\]

**Again, not worth it.**

---

## Bet 3: Scrabble Tiles

You draw 3 Scrabble tiles with replacement from a bag of 60 (18 vowels, 42 consonants). Payouts:

- 0 vowels → \$0
- 1 vowel → \$20,000
- 2 vowels → \$20,000
- 3 vowels → Lose \$90,000

Let’s compute:

- \( P(0) = \left( \frac{42}{60} \right)^3 \)
- \( P(1) = 3 \cdot \left( \frac{18}{60} \right) \cdot \left( \frac{42}{60} \right)^2 \)
- \( P(2) = 3 \cdot \left( \frac{18}{60} \right)^2 \cdot \left( \frac{42}{60} \right) \)
- \( P(3) = \left( \frac{18}{60} \right)^3 \)

\[
\text{EV} = P(1) \cdot 20{,}000 + P(2) \cdot 20{,}000 - P(3) \cdot 90{,}000 - 10{,}000
\approx +\$170
\]

**This one is actually favorable. Take the bet!**

---

## Summary

| Bet/Game              | Expected Value | Should You Take It? |
|-----------------------|----------------|----------------------|
| Coin Flip             | -\$2.50        | Nope                  |
| Lottery Ticket        | -\$1.33        | Nope                  |
| Target Shooting       | -\$8,000       | Nope                  |
| Card Bet              | -\$2,230       | Nope                  |
| Scrabble Bet          | +\$170         | Go ahead                  |

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube EZMSSMFC6UA >}}
