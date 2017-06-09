[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Design Patterns

A **design pattern** is a general solution to a commonly-occuring problem in software design and engineering

## Adapters

An **adapter** works as a bridge between two incompatible interfaces. The best way to describe how this works is through an example:

- Suppose you have a `MediaPlayer` interface that uses the class `AudioPlayer` to play audio files. By default, `AudioPlayer` can only play `.mp3` files.
- Now suppose you want to use `MediaPlayer` to call the class `AudioPlayer` but also play `.aac` files
- Suppose there also exists a class `AdvancedAudioPlayer` that can play `.aac` files.
- So you write an adapter `MediaAdapter` that will let `AudioPlayer` use `AdvancedAudioPlayer` to play more formats
- So when `MediaPlayer` calls for `AudioPlayer` to play `.aac` files, it does not need to know if can or can't play it — because the `MediaAdapter` makes it think that `AdvancedAudioPlayer` is a part of it

An adapter ensures that near-similar yet different implementations of a class can be extended upon without having to change the original class

## Model-View-Controller

- **Model** — the data you're interested
- **View** — presentation logic
- **Controller** — controls the whole thing

The **Model-View-Controller** system isn't really a design pattern, but more of an _architectural_ pattern, and it involves a non-circular dependency with low coupling.

## Vokac

**Vokac's Theory** states that:

> In any nontrivial software product, there will be areas that have an irreducible, significant complexity. Unless they are designed and maintained carefully, such areas will have higher defect rates than the average in the product

Vokac developed a tool (and conducted a study) that identifies design patterns in classes and analyses their defect rate (i.e. how often problems occur in those classes based on how often they're re-implemented). The results show that:

- The **Factory** design pattern fared the best with the least defects, due to its low-coupling
- The **Singleton** and **Observer** design patterns fared the worst, due to their large codebases and high-coupling

## “Borrowing” Solutions

- No need to re-invent the wheel: use solutions that are already out there in the community
- For example, no-need to re-think algorithms and data structures (just learn what already exists)
- Sometimes, it's even smarter to use standard algorithms (that way, people looking at the code can understand already how it works) 