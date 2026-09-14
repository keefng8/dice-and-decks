# Dice and Decks

Dice notation that actually works - 4d6kh3, 2d20adv, exploding dice - plus a card deck with draw and shuffle. For tabletop nights when the dice are in the other room.

A feature for [Mavis AI](https://www.mavis-ai.com) — a desktop voice assistant.

```
You: "open dice and decks"
```

Mavis opens it and stands its own panels down so they are not in your way. Say *"show the interface"* to bring them back.

## Install

From the Mavis Appstore — find **Dice and Decks** and click Install.

Or install it directly:

```python
from utils.feature_install import install_from_github
install_from_github("https://github.com/keefng8/dice-and-decks")
```

## What you can say

- *"open dice and decks"*
- *"roll some dice"*
- *"roll 2d20"*
- *"draw a card"*

These are not matched word for word. Mavis gives them to its language model as examples of intent, so close variations work too.

## How it works

Rejection sampling rather than `% n`, which biases the low faces, and a Fisher-Yates shuffle rather than sort(() => Math.random() - 0.5), which does not produce a uniform deck. It is a dice roller; the randomness should be right.

## Requirements

None. A single HTML file — it runs in your browser, offline, and nothing leaves your machine.

## Building your own

See [Building features for Mavis](https://github.com/keefng8/mavis-feature-docs) — a feature is just a GitHub repository with a `mavis.json`.

## License

MIT — see [LICENSE](LICENSE).
