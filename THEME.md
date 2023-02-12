__Main Foci__
-
1. Detecting weaknesses
2. Interpreting systems
3. curing systems with enriched training data - mostly optional

__Detecting weaknesses__
-
1. biases in NNs
2. detecting artifacts
  - feature based classifiers, attention or gradient based methods
3. Attacking/stress-testing systems
  - Hard test items (existing resources, specialized or filtered datasets)
  - creating variations (synonyms, paraphrases)
  - flipping and deleting tokens (permutations)
  - degenerate test settings (omitting question, premis)
4. Provide analyses of results!
  - measuring drop in performance
  - measure relative effect oif the different factors
  - qualitative analysis
 
 __Interpreting systems__
 -
 1. probing pretrained LM (0-shot) or testing fine-tuned model
 2. Approaches
  - Identifying, quantifying and visualizing parts in the input matter (GRadient, SHAP, attention)
  - Input variation (Identify parts of the input that matter by deletion, permutations, etc.)
  - Probing analysis (by MLM prediction and evaluation)
  - Compare against annotation of linguistically relevant information

__Curing systems__
-
1. Leverage knowledge from existing resources and annotated data
2. inject knowledge by recasting data
  - WordNet, FrameNet, etc.
3. Analyze the imoact of enriched training sets
  - performance differences, etc.
