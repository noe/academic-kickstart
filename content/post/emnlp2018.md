---
title: 'Notes on EMNLP 2018'
date: 2018-11-27
draft: false 
---

I recently attended the
[Empirical Methods in Natural Language Processing (EMNLP)](http://emnlp2018.org/) conference.
In this post I write about the most remarkable stuff presented there and in the co-located
events, from the point of view of a neural machine translation researcher. These are just
my opinions, feel free to disagree.

Feedback is very welcome. Please leave your comments as replies to
[this tweet](https://twitter.com/noecasas/status/1067365571661049857).

If, after reading this post, you want to know more about what happened at EMNLP 2018, I recommend
[searching for hashtag #emnlp2018 on twitter](https://twitter.com/search?q=%23emnlp2018&src=typd)
as there was plenty of live tweeting.

---

Before the main conference, there were two days of co-located events. The three most interesting
ones were the [Conference on Machine Translation (WMT)](http://www.statmt.org/wmt18/),
the [SIGNLL Conference on Computational Natural Language Learning (CoNLL)](http://www.conll.org/2018)
and the [Blackbox NLP Workshop](https://blackboxnlp.github.io/).

## WMT

[WMT](http://www.statmt.org/wmt18/) started as a workshop on statistical machine translation, with
several shared task competitions were you could take place it. [We](http://talp.upc.edu/) participated
in the [**news translation shared task**](http://www.statmt.org/wmt18/translation-task.html),
specifically in Estonian-English and Finnish-English
([our system](http://www.aclweb.org/anthology/W18-6406)).

English to German translation, and especially the WMT14 dataset, has lately become the
[standard benchmark](https://nlpprogress.com/english/machine_translation.html) for machine
translation quality (followed by English to French). This year's news translation task included
English to German and Facebook AI Research won in that translation direction with
[their massive use of backtranslation](https://research.fb.com/publications/understanding-back-translation-at-scale/).
In general, the [Transformer model](https://arxiv.org/abs/1706.03762) was dominant architecture in the news
translation task, with a special mention to [Marian](https://marian-nmt.github.io/) implementation,
which seems to be gaining momentum due to its
[very high performance](https://marian-nmt.github.io/features/#benchmarks).

You can check the full [WMT18 news translation task findings report](http://aclweb.org/anthology/W18-6401.pdf)
for all the details of the competition.

----

Apart from the news task, this year I found interesting the
[**noisy corpus filtering task**](http://www.statmt.org/wmt18/parallel-corpus-filtering.html).
Partitipants were
provided a huge corpus, for which they have to score each sentence pair. Based on the scores, the
organization sampled one smaller and one larger subset and trained statistical and neural MT system
and evaluated the translation quality. I think it's worth mentioning Microsoft's
[Dual Conditional Cross-Entropy Filtering](http://aclweb.org/anthology/W18-6478), which seemed to be
simple yet very effective.
The full report of the corpus filtering task is [here](http://statmt.org/wmt18/pdf/WMT081.pdf)

## CoNLL

I could not attend [CoNLL](http://www.conll.org/2018), but I would like to mention the article
that won the best paper award:
[Uncovering Divergent Linguistic Information in Word Embeddings with Lessons for Intrinsic and Extrinsic Evaluation](http://aclweb.org/anthology/K18-1028),
which proposes a method to adapt pretrained embedding vectors to work better for 
semantics/syntax tasks or for similarity/relatedness tasks.

## Blackbox NLP

EMNLP stands for "Empirical Methods...". The incorporation of the deep learning black box into NLP has
lead to an emphasis in the empirical part, ruling out most of the interpretability derived from
symbolic approaches and from the modular structure of statistical methods.
Many pieces of research just try to characterize the behaviour of models and the
effects observed when they are subjected to
explorative experiments, but the analyses undergone to explain them are sometimes superficial or
are merely justified by intuition, and there are few conclusions that can be applied to contexts
other than those very specific experiments.

[Blackbox NLP Workshop](https://blackboxnlp.github.io/) tried to shed some light on
the inner working of deep NLP models. The workshop gained a lot of attention, with
both the oral sessions and the poster sessions being packed.

Despite the attempts to make NLP neural networks more interpretable, I think that
the _black box nature_ of the currently dominant models imposes a hard non-interpretability wall
that prevents us from actually understanding their behaviour completely, and hence we just can
resort to characterizing them under different conditions.
I hope that at some point we devise models with built-in interpretability where
we no longer need to trade interpretability for effectiveness.

## EMNLP: Main Conference

Unsupervised Statistical MT techniques were presented by the
[Basque Country University](http://aclweb.org/anthology/D18-1399)
and by [Facebook AI Research](http://aclweb.org/anthology/D18-1549), achieving
astonishing result without a single pair of parallel sentences.

The trend from last conferences to try to leverage linguistic knowledge was not
very strong at EMNLP. The most remarkable articles were
[Linguistically-Informed Self-Attention for Semantic Role Labeling](http://aclweb.org/anthology/D18-1548)
and
[On Tree-Based Neural Sentence Modeling](http://aclweb.org/anthology/D18-1492).

Cross-lingual learning was present in a lot of different articles
presented at the conference, both regarding word embeddings, machine
translation. You can take a look at the [accepted papers](https://aclanthology.coli.uni-saarland.de/events/emnlp-2018)
and search for "cross-lingual" to get an idea.

The recent enthusiams about transfer learning with pretrained models like
[ELMo](https://allennlp.org/elmo), 
[BERT](https://arxiv.org/abs/1810.04805) and
[ULMFiT](https://arxiv.org/abs/1801.06146) was not reflected at EMNLP, but will probably do
at next conferences, for which there's still time to build new systems making use of them.

## Summary highlights


- Transformer and backtranslation are the standard machine translation toolbox.
- Cross-lingual and low resource scenarios are gaining momentum.
- Currently, unsupervised SMT works better than unsupervised NMT.

