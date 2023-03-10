__NERC of different granularities__
-
  - Think of settings for probing and fine-tuning with a MLM
  - compare to SOTA systems
  - perfomr model inspections (what information does the model rely on for prediction?, dataset biases?)
  - How to recast Data for NER?
  - How to cope with multi-word NEs? (BERT applies single token masking)
 
 __Word Sense disambiguation__
 -
  - Think of ways to perform WSD with a PLM (WSD as probing task)
  - WSD in fine-tuning setting (use training corpus for fine-tuning, compared to probing?)
  - Model inspection (on what does the model base its predictions?)
  - REcast datasets
  - WSD in an unsupervised manner (by clustering e.g)
  - benchmarks and leaderboards

__Semantic protorole labeling__
-
  - Semantic proto-roles (as sets of entailment that arguments must satisfy)
  - Can we assign roles using NLI and role-specifix hypotheses?
  - fine-tune on SPRL data
  - Recast data from PropBank SRL training data

__FrameNet SRL or QA-SRL__
-
  - alternative
  - similar to SPRL and ORL, semantic argument role labeling can in general be framed as NLI
  - FrameNet provides role definitions --> can be used as hypothesis!
  - QA-SRL uses nl to annotate semantic roles
  - generate verb-specific questions --> the answer identifies the argument!

__Semantic textual similarity <3__
-
  - Sentence representation learning
  - Use PLM to predict sent simil
  - Compare perfomrnace of 0-shot vs. fine-tuning
  - Data Sets: STS Shared task dataset; PAWS Paraphrase adversaries from Word Smapling

__Discourse relation sense classification__
-
  - sentences in coherent discourse are related (by way of a Discourse Marker _explicit_; no DM _implicit_)
  - Penn Discourse Tree Bank --> annotates DRs of both types with a coarse-to-fine-granied relation inventory
