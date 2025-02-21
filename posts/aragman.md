---
title: "a rag man"
subtitle: "The world's first fun anagram tool."
categories:
    - projects
draft: true
---

I made "a rag man" because the other anagram websites I found are focused on finding complete single-word anagrams, typically using the scrabble worldlist, often explicitly to win at word games. This both misses the point of games and also squanders the fun of anagrams.

This led me to build the site / word-toy "a rag man". It allows you to iteratively build multi-word anagrams. It also allows you to add and use any arbitrary nonsense word you want. If there's some slang you find funny or meaningful, or a missing word, go ahead, throw it in.

## Funny Little Anagrmas

## Other Features!

- Optimized for sharing, option panel, etc. finish this section

## Implementation Details (Boring)

### Algorithms and LLMs

The classic way to solve these anagram problems is using some kind of [Counter]()-like structure. However, I wanted to all substring anagrams. This is basically a permutation problem, and calculating permutations is incredibly slow. We could use caching, but why do that when you can just write a good algorithm instead? What I did was first, get a word list, then create a word map from it where the key is the sorted characters, and the value is an array of all the words that correspond to that sorted string. Then, sort the input and then just write an algorithm to look up all the valid [combinations]() and return those. This lowers our running time from O(n!) to O(2^n). That's uh, basically good! TODO: include a graph or something.

This algorithm was apparently incomprehensible to any LLMs I showed it to. I consistently have this issue with recursive algorithms that are not widely used in Leetcode problems, and even some that are! Part of the issue might have been that I was doing something a little atypical with anagrams.

### Frameworks, Languages

I used React for a couple reasons. First, I had to use it professionally, so I already know it. Second, I wanted it to be able to work entirely client-side and offline (though I know there are other ways to do this). Finally, it seemed like a natural fit for a small stateful app. I thought it would be pretty pleasant without all the Redux store nonsense, there shouldn't be a huge mess of hooks. I wanted to give React an opportunity to really shine. It was... only okay! Kind of annoying. I experienced the standard annoyances with managing state and triggering/avoiding rerenders, and surprisingly, even race conditions. I ironed those out, but sometimes it still does the ol' React flicker, which I don't really want to spend a ton of time ironing out.

Recently I also dedicated a whole day to making a CRUD app with Streamlit, a technology I had never interacted with until that day. I managed to ship an MVP the same day. Another win for the one-day-one-project method. I expected it to be totally smooth sailing, but instead I had to fight some of the same battles with state and rerendering. There were no race conditions, except now there had to be some server actively running Python, which makes serving it much more of a pain. I think a lot of these issues are just inherent to this sort of rerendering stateful app, Streamlit made React look good, but that's not a ringing endorsement of either.

