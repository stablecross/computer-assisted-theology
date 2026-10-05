# computer-assisted-theology

Theology argued from Scripture, reviewed by AI models under published criteria. Bug reports welcome.

## What this is

This repository holds theological papers written the way software is written.

Each paper states its claim at the top and argues it step by step. Its premises come from Scripture and from the conclusions of earlier papers, which it names. Each step of the main argument is numbered, so a reader can point to the exact step that fails. Objections and supporting material are in named sections.

Each paper is then tested. The tests are reviews by AI models working under published criteria, described below. A defect found by a reviewer is logged, and the paper is corrected in a new version.

## Why

Mathematics has already made this move.

For most of its history, a proof was checked by other mathematicians reading it. In the 1960s and 1970s, the first computer programs were written to check proofs mechanically.

In 1976, Kenneth Appel and Wolfgang Haken proved the four-color theorem: any map can be colored with four colors so that no two neighboring regions share a color. The computer did two jobs in that proof.

- **It checked the proof.** It worked through about 1,500 cases that no person could check by hand.
- **It helped build the proof.** For two years their program took in their ideas and tested them, and its results guided how they revised the argument. They wrote that the program "began to surprise us."

Many mathematicians refused to accept a proof they could not check by hand. In 2005, the whole proof was checked again, step by step, by a proof-checking program. Today AI models help mathematicians both find proofs and check them.

This repository follows both parts of that example. The papers were drafted with computer assistance, and they are tested by computer review. The author is responsible for every claim in them.

## Why theology has not made this move

Mathematics can be checked by machine because it fixes three things in advance:

- each symbol has one meaning;
- a base set of truths, the axioms, is stated;
- the operations allowed on each symbol are specified.

So a program can check a mathematical proof by applying the rules, without judging what the symbols mean.

Words do not have that fixity. The same word can carry different meanings, and its context decides which one it carries. For example, Paul uses "flesh" for bodily life in Galatians 2:20 and for human nature set against God in Romans 8:8. So the meaning of a text cannot be looked up. It has to be judged as the most likely meaning in its context.

The AI models used here are large language models (LLMs), and they are built for that task. Such a model is trained on a vast body of text to predict what comes next. To do that well, it has to judge which meaning a word most likely has in its context. That is the skill a reviewer of a theological argument needs.

A theological argument is a long chain of inferences from texts. One step that does not follow breaks the chain. Human reviewers are few and slow, and most come to an argument having already accepted or rejected its conclusion. An AI model can read the whole chain and test each step against a published standard. It does not tire, and it can be run again after every revision. (The first evaluations of the four papers in [abrahamic-covenant/](https://github.com/stablecross/computer-assisted-theology/tree/main/abrahamic-covenant) and [ezekiel/](https://github.com/stablecross/computer-assisted-theology/tree/main/ezekiel) by GPT-6.1 Sol at maximum effort took two hours in all.) So a paper can be tested the way code is tested: checked again after every change.

## What this does not claim

Theology is not mathematics. The premises are texts, and reading a text is not a deduction. So these papers are not proofs, and a passing review does not make a conclusion true.

AI models are imperfect reviewers. They miss real errors. They also report errors that are not there. Different models reach different findings, and a model's findings change from one version to the next. One model's review can lead another model to revise its own. A more capable model may find what earlier models missed, and the review cycle then starts again. The models may never fully agree with one another.

So agreement among models is not the test. A reviewer's finding is itself tested: the criteria require whoever reports a defect to demonstrate it.

A model's answer can be steered by how the question is asked. The same is true of people. So the review prompt is fixed and published, and it asks only whether each step follows, not whether a conclusion is true. Anyone can rerun it, on any model, or with a prompt aimed at refuting the paper. A finding counts only if its reason holds under the criteria, using nothing the corpus does not supply. That rule binds a human reviewer as much as a model.

This is not an attempt to train an AI model to a theological system. Any model can be trained to give answers congenial to a particular system. The models here are not taught what to conclude. They are asked whether each step follows from the texts and steps before it. The goal is inference, not pedagogy.

## How the papers are tested

### How a paper is laid out

A paper that argues from the text opens with front matter: its claims, its terms, its imports, and what it does not argue. The front matter also says what an objection has to do. For each claim, it states what an objector would have to show to defeat it.

That section comes before the argument on purpose. It is the test written before the code. The conditions for failure are fixed before the argument runs, so they cannot be shaped afterward to fit what the argument managed to show. The criteria work the same way: the burden of proof is set first, and the evidence is weighed after.

So the section names texts and steps the reader has not reached yet. On a first reading, skip it and come back to it after the argument. Near the end of the paper, "What is inferred, and where to attack" ties the same conditions to the steps they apply to.

### The corpus

[corpus.md](https://github.com/stablecross/computer-assisted-theology/blob/main/corpus.md) states the premises: the sixty-six books of the Protestant canon, the text quoted, and the method assumptions. A reviewer who does not accept the corpus says so, and may go on only with a conditional review: *given this corpus, the argument establishes X.*

### The criteria

[criteria.md](https://github.com/stablecross/computer-assisted-theology/blob/main/criteria.md) holds the four-stage evaluation criteria for reviews. Papers are tested under its latest version.

A review runs in four stages, and each stage asks one question:

1. **Logic.** If every premise is granted, does the conclusion follow?
2. **Exegesis.** Do the cited texts say what the paper says they say?
3. **The rest of Scripture.** Do texts the paper does not cite overturn it, or support it?
4. **Consequences.** If the conclusion stands, what follows from it?

### Why the criteria are built this way

The stages are kept apart because each kind of objection has to be answered in its own terms. A valid argument is not invalid because a reviewer dislikes its consequences. So consequences are weighed last, at Stage 4, and may never be used as evidence at Stages 1 through 3.

The criteria also separate what an objection shows. An objection is classed as one of three results:

- **Refutation.** It shows the conclusion is false.
- **Failure of the offered proof.** It shows the argument does not establish the conclusion. It does not show the conclusion is false.
- **Local correction.** It defeats or narrows one step, and the conclusion still stands on the rest.

A review reports only the result its objection shows. A gap in one step is not reported as a refutation of the paper.

Possibility is not evidence; call this the possibility rule. A reading may not be saved, and an argument may not be defeated, by a premise the texts leave open but do not support. Such a premise is not declared false. It is unavailable, and neither side may build on it.

### How the criteria were made fair to author and reviewer

The criteria have been revised many times. AI models have reviewed the criteria themselves, and where a rule was found to favor the author or the reviewer, it was rewritten. Author and reviewer are held to the same standard of proof. Four rules show the result:

- **The same rules bind both sides.** Whoever asserts a claim must support it. Whoever challenges a claim must demonstrate the defect. A reviewer's findings are claims too, and they are tested by the same rules.
- **The possibility rule cuts both ways.** A reviewer may not save an objection with an unsupported premise. The paper may not save its own reading that way either. A ruling that rejects an objection for relying on an unsupported premise must also show that the paper's own premises are better supported.
- **Support is graded like attack.** A text that seems to count against the paper is ranked on a scale from fatal to neutral. A text that seems to count for the paper is ranked on a matching scale, so support is not waved through while attacks are sifted.
- **A proof objection and a competing reading carry different burdens.** A reviewer who shows a gap in the paper's argument need not offer a rival reading. A reviewer who offers a rival reading must argue it as a proof of its own, under the same tests. Showing a gap does not establish the rival reading, and answering the rival reading does not close the gap.

### How strict the criteria are

Particle physics sets a high bar for announcing a result. A new particle is announced as a discovery only at five sigma. At five sigma, the chance that background noise alone would produce a signal that strong is about one in 3.5 million. A weaker signal, at three sigma, is reported as evidence, not as a discovery.

The bar is high on purpose. Some real effects go unannounced until the data reach it. Physicists accept that, because a false announcement does more harm.

The criteria hold conclusions to the same kind of bar. Reading a text is a judgment of its most likely meaning, as described above, so any one reading can be wrong. A conclusion built on such readings is therefore probable, not certain. So it needs a bar for when to call it established. Each review ends with the standing of each thesis: Established, Supported, Not shown, or Refuted. Established is the counterpart of discovery. The argument is valid, its necessary premises hold, and no coherent reading of the relevant texts explains them while the thesis is false. Supported is the counterpart of evidence. The thesis is better supported than its strongest rival, and the rival is not excluded. The criteria assign no number. The comparison is to where the bar is set, not to how it is measured.

So a conclusion that falls short of Established is not thereby false. Only Refuted means false. Readers on every side will find that something they believe falls short. That is a result of the bar, not a verdict on the belief.

## Usage

To review a paper, give an AI model these files:

- the paper;
- [criteria.md](https://github.com/stablecross/computer-assisted-theology/blob/main/criteria.md);
- [corpus.md](https://github.com/stablecross/computer-assisted-theology/blob/main/corpus.md);
- every paper it imports, as listed in its folder's README.

Attach the files rather than linking to them. Some models cannot fetch web pages, and others fetch GitHub's page around the file instead of the file itself. A paper and its imports can run to 75,000 words, which fits in the largest models' context windows but not in every free tier.

Then use this prompt unchanged:

> Evaluate the attached paper under the attached criteria. The agreed corpus is stated in the attached corpus.md. If the paper imports conclusions from other papers, those papers are also attached; test the paper's use of them, not the imports themselves. Report each stage separately. End by stating the paper's version, the criteria version, and the corpus version.

The prompt names the files and nothing else. It does not ask the model to find flaws or to confirm the argument; how hard to push is set by the criteria. Using the same prompt makes reviews comparable, so differences between reviews come from the models and not from the wording.

A review of a paper that imports others gives a standing that holds only if the imports hold, such as "Established, given its imports." Each import gets its own standing in its own review. The paper then stands no higher than its weakest import. For example, if calvinism.md is Established given its imports, and one of those imports is only Supported, then calvinism.md is Supported.

Record the model, its version, and the date yourself. A model's report about itself is unreliable: in trials, one model gave a date two years in the past, and another said its own version was not visible to it.

Model size matters. In one trial, a model small enough to run on a laptop (an M5 Max MacBook Pro with 64 GB of memory) reached the same verdict as a larger model but found no defects. It did not state the strongest objections, and it applied the rules to the objections but not to the paper. A review that finds nothing is not evidence that there is nothing to find.

A finding you believe is correct can be filed as a bug report.

### When two papers conflict

Suppose systemA.md and systemB.md argue theses that cannot both be true, and each has been reviewed as Established. Then at least one review is wrong. Established means no admissible countermodel survives, and each paper is a countermodel to the other. So a paper's standing holds only until it is reviewed against any paper that contradicts it.

Two Established papers can conflict for three reasons:

- **They rest on different corpus or method assumptions.** The pre-analysis of each review records these. If they differ, the dispute is about what counts as evidence, and neither review binds the other side.
- **They do not actually contradict.** A key term such as "election" or "grace" may carry a different sense in each. Then both can stand, about different claims.
- **Neither review faced the other paper.** Each reviewer built its own countermodel, and neither tested the other paper's best case.

To resolve the conflict:

1. **Find where the papers collide.** Name one thesis in each paper that cannot hold together with the other, in the same sense. Follow each paper's imports back to the earliest paper whose thesis is in conflict. A later paper's standing is capped by its imports, so settling the earliest conflict settles the later ones.
2. **Write a question file.** It quotes the two theses, each with its paper and step, says that they cannot both hold, and asks for the standing of each. It adds no argument. If it argued, it would be a third paper with its own author.
3. **Attach the question file, criteria.md, corpus.md, the two papers in conflict, and their imports.** Attach only the papers that carry the conflict, not every paper that depends on them.
4. **Use this prompt unchanged:**

> Evaluate the attached question under the attached criteria. The agreed corpus is stated in the attached corpus.md. The question states two theses that cannot both hold. Each is argued in an attached paper, whose imports are also attached. Treat each paper as the other's competing reading, and test both by the same rules. Report each stage separately. End with the standing of each thesis, and name the data on which the comparison turns.

The review can end three ways. One thesis is Established and the other drops. Both are Supported, and one is ahead on named data. Or both are Not shown, which means the corpus does not settle the question. The third is a legitimate result: the bar exists so that the method says so when the texts do not decide.

Particle physics has a precedent. In 2011 the OPERA experiment reported neutrinos arriving faster than light, at six sigma, above the threshold for a discovery. Because the result conflicted with relativity, its authors presented it as an anomaly to be checked. The checks found the main cause, a faulty fiber-optic connection in the timing system. Later measurements, OPERA's among them, found the neutrinos traveling at the speed of light. A high bar does not guarantee that a result is true. A conflict says to look for an error. It does not say which result has it. Finding the error takes checking each result, which is what the joint review does.

## How to report a bug

Open an issue. Name the paper, its version, and the step.

Say which kind of defect you are reporting:

- **The step does not follow.** The conclusion of the step is not entailed by what comes before it.
- **A premise is not warranted.** The step relies on something the corpus does not state, entail, or warrant elsewhere.
- **A quotation is wrong.** The text quoted does not match the NRSV (1989), or the Hebrew or Greek does not say what the paper says it says.
- **A competing reading.** A different reading of a text fits the evidence at least as well. You must show that the reading is warranted by the corpus, not merely possible.

Show the defect. "This step seems weak" is not a bug report. "Step 7 needs X, and X is not in steps 1–6 or in the corpus" is.

Reports produced with an AI model are welcome. Say which model and version you used.

## Credits

The papers were drafted and revised with Claude (Anthropic), mostly Claude Opus up to version 5.5, with some runs on Claude Fable. Claude did most of the drafting, the revision after each review, and the checking of quotations against the NRSV.

The papers were reviewed by GPT (OpenAI), up to GPT-6.1 Sol at maximum effort, and by Grok (xAI), up to Grok 4.6. Claude did a few review runs early on. The remaining reviews came from models other than the one that drafted the text.

The author is responsible for every claim in the papers.

## Cite

Use "Cite this repository" in the sidebar for APA or BibTeX. If you cite a single paper, give its title and the version number stated at its top.

## License

Copyright © 2026 William R. Felts III. The papers are licensed under CC BY-ND 4.0: you may copy and share them, with credit, but may not distribute altered versions. See [copyright.md](https://github.com/stablecross/computer-assisted-theology/blob/main/copyright.md) and [LICENSE](https://github.com/stablecross/computer-assisted-theology/blob/main/LICENSE).

Scripture quotations in the papers are from the New Revised Standard Version (1989); the permission notice is in each paper and in [copyright.md](https://github.com/stablecross/computer-assisted-theology/blob/main/copyright.md).
