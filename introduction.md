
# Introduction

*Logical languages*, also known as *loglangs*, are a type of [constructed language](https://en.wikipedia.org/wiki/Constructed_language), specifically of [*engineered language*](https://en.wikipedia.org/wiki/Enginereed_language) (*engelang*); loglangs are characterized by being primarily concerned with syntactic unambiguousness and foundation on formal logic.
Different loglang projects may have different standards on what exactly constitute ‘syntactic unambiguousness’ (also called “monoparsing”, or “monosyntacticity”), some with more strict and stringent constraints than others.
Mature loglang projects feature one or several parsers — pieces of software for parsing utterances and texts in the language, outputing more or less detailed syntax trees, possibly with additional features such as glossing and [formal semantics](https://en.wikipedia.org/wiki/Formal_semantics) denotation of the syntax tree, as well as translation to some sort of logic notation.
By virtue of syntactic unambiguousness, such a parser may not output more than one single syntax tree for any given input utterance in the language.

In order to achieve the goal of syntactic unambiguousness, including unambiguousness of productive word-internal structures and morphology, word morphology needs to comply to the concept of [‘self-segregating morphology’](https://tmh.conlang.org/self-segregating-morphology/), often shortened as ‘SSM’. This not only ensures that words can be unambiguously segmented into their productive subcomponents (roots, productive derivational affixes, inflectional affixes…), but also that boundaries between individual words also be unambiguous, such that an utterance can always be segmented into a single unambiguous stream of words.

Besides the target goal of syntactic unambiguousness, loglangs often feature additional goals, most often the avoidance of lexical ambiguities (homonymy, polysemy not resolvable by the surrounding syntax) even when they are not source of syntactic ambiguities, as well as the goals of grammatical simplicity and exceptionlessness. Some of them also pursue the goal of greater precision and crispness in lexicosemantics (meanings of the language's lexical units).

With respect to the kind of lexical ambiguities which loglangs typically strive to avoid, what is targeted is not semantic broadness, vagueness or abstractness, as for example with the word “animal” which is more vague and abstract than “cat” or “dog”, but rather what is targeted is homonymy-like ambiguousness, when a single word or lexical unit has two or more distinct meanings, but *cannot manifest them all simultaneously*, as with the word “bat” in English, which can either denote a flying mammal or a baseball stick, but cannot mean both at once in a single utterance, for “there are two bats in the room” cannot mean that there's one flying mammal and one stick in the room.
On the other hand, semantic broadness (as with “animal”) is not ambiguity, and is actually a very desirable property of language (allowing for generalization). Arguably, a language without semantic broadness would be practically unusable, as nouns would be like proper names, each referring only to a single concrete individual, instead of abstract classes of individuals.

Finally, while this has technically little to do with loglanghood itself, most of the current loglang projects are verb-only languages (except possibly for pronouns) or have a single open flexible part of speech, able to act either as verbs or nouns depending on the situation or morphological inflection. Additionally, none of them have mandatory number marking (i.e. ‘singular’ vs ‘plural’) except for Toaq in personal pronouns.


# Main current loglang projects

## Toaq

[Toaq](https://toaq.net/) is a loglang by Hoemaı, initiated in 2013, with the latest major revision (*Toaq Delta*) released in 2022, is a loglang with East Asian aesthetics, featuring grammatical tone inflection, almost no other form or inflection except for a few inflectional prefixes, productive derivational prefixes, serial verb construction and verb-initial word order among other features. It strives to avoid so-called *‘terminators’* for demarcating the boundaries of phrases and subordinate clauses (with the exception of quotes and parentheticals), instead relying on *valency saturation* for determining where a phrase becomes complete (*saturated*) and therefore ends.
With respect to the lexicon, the language makes much more parsimonious use of argument slots, and strives to keep valency to a minimum, avoiding all slots that are not strictly necessary, unlike the tradition in first-generation loglangs like Loglan and Lojban. Toaq verb valency is limited to a maximum of 3. Words are often of *‘a priori’* origin, without relation to words in other languages, although there are cognates or borrowings from a number of natural languages and also a few from Lojban. Compound words are extensively used. Toaq currently enjoys a lexicon of more than 20k lexical units.

The main Toaq parser is [Kuna](https://toaq.net/kuna/), it is currently the most advanced parser of all loglangs. In addition to linguistic syntax trees, it also does step-by-step compositional semantic denotation of the trees, showing how the meaning (as expressed in a custom logic notation) of each phrase is composed from the meanings and types of the elements that constitute it.

## Lojban

[Lojban](https://www.lojban.org/) is historically the second loglang to have been created, made in 1989 as a relexified fork of the Loglan language (the first loglang). It is a verb-only language (besides a closed class of pronouns), lacking any form of morphological inflection, but featuring an complex and intricate morphology, featuring compound words made of irregularly reduced root forms. For expressing the equivalents of nouns, Lojban makes extensive use of determiner phrases acting like reduced relative clauses, where a determiner introduces a verb as the descriptor of its referents (for example, ⟪su'o mlatu⟫, composed from ⟪su'o⟫ “some” + ⟪mlatu⟫ “to be a cat”, means “some cat”, “something that is a cat”). In addition, it features *elidible terminators*, i.e. particles that demarcate the end of a phrase when its absence would cause following words to be incorporated into that same phrase. Lojban has a very rich (arguably *overly* rich) collection of grammatical particles, many of which are uncommon or rarely used if at all.

The Lojban lexicon features [bloatedness of verb frames](<https://mw.lojban.org/papri/Bloated_Gismu_Syndrome>) (argument structures), most verbs having unnecessary auxiliary argument slots indicating function, standards, conditions of truth, material composition, and many other such things. Verb frames are often irregular and inconsistent, verbs of similar meanings often have inconsistent frames (slot types, slot ordering, valency…). This is occasionaly source of semantic issues, as with the tetravalent verb ⟪botpi⟫, defined as *“x₁ is a bottle for containing x₂, made of x₃, with lid x₄”*, implying that a bottle without associated lid cannot be described as being a ⟦botpi⟧. Lojban does not put a limit on the valencies of verbs, except for the core set of basic verbs called *“gismu”*, which have a maximal valency of 5 (with the exception of a very few ones allowing infinite valency). Simiarly to Toaq, Lojban's lexicon contains a little over 20k lexical units.

Lojban has undergone significant dialectalization over time. There exist various parsers for Lojban, such as [this one](<https://lojban.github.io/ilmentufa/glosser/glosser.htm>) and [that one](<https://lojban.github.io/ilmentufa/camxes.html>). There exist parser versions specific to certain dialects.


## Loglan

[Loglan](<http://www.loglan.org/>), created in 1955 by the sociologist James Cook Brown, is the first constructed language to have been qualified as ‘logical language’, and it is historically the ancestor of Lojban. As it has since continued to evolve separately, it may also be qualified of sister language to Lojban. Lojban started off mostly as a relex of Loglan. While the two languages retain strong similarities, they have slowly drifted away from each other. Loglan has a little over 10k lexical units.

## Xextan
[Xextan](https://xextan.github.io/), released in 2022, started as a drastic simplification of Lojban, with shortened, monosyllabic verb roots instead of the Lojban disyllabic roots. Xextan aims at simplicity and ease of learning. It currently has 1115 words.

## Eberban
[Eberban](https://eberban.github.io/eberban/), released in 2020 by Mia Entropy, is a verb-only loglang whose grammar revolves around the concept of [serial verb construction](https://en.wikipedia.org/wiki/Serial_verb_construction); the concepts of nominalization, noun phrase and determiner phrase don't exist in Eberban, everything is expressed as a chain of verbs, each having certain inherent syntactic behaviors such as intransitivity vs transitivity, as indicated by the shape of the verb word. Eberban currently has 774 words.

## Nahaıwa
[Nahaıwa](https://ntsekees.github.io/), released in 2021 by Ntsékees, is a polysynthetic loglang with a complex inflectional morphology, with word stems inflecting for many possible syntactic functions such as root verb (with illocution marking), subordinate verb, noun (with noun case marking), adjective, adverb, interjection, and even coordinator and quantifier. The language only has a very few particles (not even a dozen), as most of the grammatical load is assumed by the morphology. The language currently has 450 lexical units.

## Gua\spi
[Gua\spi](https://www.jfcarter.net/~jimc/guaspi/), released in 1989 by Jim F. Carter, was historically the 3rd loglang project, and the first tonal loglang. It features syllabic consonants, grammatical tones allowing navigating in abstract levels of syntactic nesting, as well as extensive use of type correction.

## Others

# Loglangology resources

## Predilex: a cross-loglang lexicosemantic thesaurus

[Predilex](https://ntsekees.github.io/Predilex/viewer/index.html) ([🔗 repository](https://github.com/Ntsekees/Predilex/)) is a thesaurus of sememes represented as predicates, each bearing an unique ID, with definitions in English and logic notation, as well as cross-linking with lemmas in various natural language and logical languages; it also features semantic category tags and relationships like hypernymy, meronymy etc. with other Predilex entries.

## Loglang Tatoeba
[Loglang Tatoeba](https://ntsekees.github.io/loglang-tatoeba/) ([🔗 repository](https://github.com/Ntsekees/loglang-tatoeba/)) is a repository of challenging English sentences with translations in various loglangs and other languages. One of its purposes is to showcase the solutions that have been found for translating such sentences in loglangs.


