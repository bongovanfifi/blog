---
title: "a rag man"
subtitle: "The world's first fun anagram tool."
categories:
    - projects
---

I made ["a rag man"](https://aragman.futz.zone/) because the other anagram websites I found are focused on finding complete single-word anagrams, typically using the scrabble worldlist, often explicitly to win at word games.

This led me to build the site / word-toy "a rag man". It allows you to iteratively build multi-word anagrams. It also allows you to add and use any arbitrary nonsense word you want. If there's some slang you find funny or meaningful, or a missing word, go ahead, throw it in.

## Funny Little Anagrmas
Here's a list of funny little anagrams my friends have found for their names, occasionally I'll update these.

- Dinky Leprosy Oaf
- Silly Cannon
- Outdrank a Genie

## Implementation Details (Boring)

### Algorithms and LLMs

The classic way to solve these anagram problems is using some kind of [Counter](https://docs.python.org/3/library/collections.html#collections.Counter)-like structure. However, I wanted to get all substring anagrams. This is basically a permutation problem, and calculating permutations is really slow, O(n!) time. We could use caching, but why do that when we can just write a good algorithm instead? I take the word lists and create word maps where the key is the sorted characters, and the value is an array of all the words that correspond to the word sorted. Then, I just sort the input and write a combination algorithm O(2^n) and return those.

### Frameworks, Languages

I used React for a couple reasons. First, I had to use it professionally, so I already know it. Second, I wanted it to be able to work entirely client-side and offline (though I know there are other ways to do this). Also, it seemed like a natural fit for a small stateful app. I thought it would be pretty pleasant without all the Redux store nonsense, this would be an opportunity for React to really shine. It was... only okay! Kind of annoying. I experienced the standard annoyances with managing state and triggering/avoiding rerenders, race conditions. Honestly, a lot of these annoyances are just inherent to this sort of reactive application.

