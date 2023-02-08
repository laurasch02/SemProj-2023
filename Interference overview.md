__Quantifiers__
-
- How well does a PLM capture non-monotonicity? (Useful 0-shot MLM or NSP formulation?)
- On what basis does a pre-trained or fine-tundes model make predicitons? (Where and how do the models fail with hard data?) (Analyze failure and successes and underlying training and test sets!)
- Can you extend data sets with uncovered phenomena? (What about verb entailments or cardinality? Consult the FraCast test suites for phenomena)
- Monotonicity Entailment Dataset (MED)

__Fine grained evaluation of NLI capacities__
-
  - fine-tune a PLM (BERT, RoBERTa, BART, ...) for NLI --> BART eher nicht, oft nicht unterstützt!
  - using extended datasets
  - Why do PLMS not perform well on NLI 0-shot testing?
  - Does system analysis for fine-tuned models confirm that your model makes the right predictions for the right reasons?
  - How to make use of data from WordNet, FrameNet, etc.?
  - Does fine-tuning on data from linguistic resources improve perfomrance?
  - Does model analysis confirm that you get improvements for the right reasons?
  - Hard NLI Datasets
  - Veridicality
  - Factuality (FactBank)
