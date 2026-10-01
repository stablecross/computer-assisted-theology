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

This is not an attempt to train an AI model to a theological system. Any model can be trained to give answers congenial to a particular system. The models here are not taught what to conclude. They are asked whether each step follows from the texts and steps before it. The goal is inference, not pedagogy.

## How the papers are tested

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

## Usage

To review a paper, give an AI model these files:

- the paper;
- [criteria.md](https://github.com/stablecross/computer-assisted-theology/blob/main/criteria.md);
- [corpus.md](https://github.com/stablecross/computer-assisted-theology/blob/main/corpus.md);
- every paper it imports, as listed in its folder's README.

Attach the files rather than linking to them. Some models cannot fetch web pages, and others fetch GitHub's page around the file instead of the file itself. A paper and its imports can run to 75,000 words, which fits in the largest models' context windows but not in every free tier.

Then use this prompt unchanged:

> Evaluate the attached paper under the attached criteria. The agreed corpus is stated in the attached corpus.md. If the paper imports conclusions from other papers, those papers are also attached; test the paper's use of them, not the imports themselves. Report each stage separately. End by stating the paper's version and the criteria version.

The prompt names the files and nothing else. It does not ask the model to find flaws or to confirm the argument; how hard to push is set by the criteria. Using the same prompt makes reviews comparable, so differences between reviews come from the models and not from the wording.

Record the model, its version, and the date yourself. A model's report about itself is unreliable: in trials, one model gave a date two years in the past, and another said its own version was not visible to it.

Model size matters. In one trial, a model small enough to run on a laptop (an M5 Max MacBook Pro with 64 GB of memory) reached the same verdict as a larger model but found no defects. It did not state the strongest objections, and it applied the rules to the objections but not to the paper. A review that finds nothing is not evidence that there is nothing to find.

A finding you believe is correct can be filed as a bug report.

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
