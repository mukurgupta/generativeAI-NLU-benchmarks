## Modern LLM Benchmarks

### Common Sense Reasoning:
1. **BoolQ** - Binary question ansering task. Each example contains (question, passage, answer). Typically formulated as text-pair classification task. Current SOTA is ST-MoE-32B followed by finetuned PaLM 540B and T5-11B.
2. **PIQA** - Physical common sense reasoning QA dataset - Physical Interaction: Question Answering. Each example contains a question (pertaining to everyday activities) and two choices for solutions. System must identify the right solution for the task in the question.
3. **SIQA** - Question answering benchmark for social commonsense intelligence - Social Interaction: Question Answering. Each example contains a context string, a question and 3 choices for answers. System must identify the right answer from the given 3. LLaMA 65B is SOTA followed by Chinchilla, Gopher and LLaMA 13B,33B and 7B.
4. **HellaSwag** - Commonsense natural language inference dataset - given some context complete the sentence. Considers real life situations and make predictions on what might happen next. Each example has a string (some context + an incomplete sentence) and 4 choices for what might happen next. System is asked to predict the right choice. Dataset created by Adversarial Filtering - wrong model generated answers are selected specifically.
5. **WinoGrande** - Commonsense fill-in-the-blank task. Each example has a sentecen with a blank along with 2 possible choices for the blank. System is requred to select the right option for the blank.
6. **ARC** - Grade-school level multiple choice science questions. Partitioned into Easy and Challenge sets. Each example has a science question and 4 possible choices for the answer.
7. **OpenBookQA** - Contains questions along with the required domain fact to answer the question. Contains tricky questions that require multi-step reasoning and use of additional commonsense. Each example has a question, fact, human difficulty score and 4 choices for the answers. System is required to select 1 of the four given choices.
8. **StoryCloze** - 

### Closed-book QA

9. **Natural Questions** - Contains natural user questions from Google search and corresponsing wikipedia page which may or may one contain the answer. Each wikipedia page maybe annotated with long and short spans. Longer ones may contain the answer and shorted ones may contain the specific answer. Each example has a user question, wikipedia page, corresponding long and/or short annotations of the answer if present. Problem may be formalted as an extractive QA.
10. **TriviaQA** - : Reading comprehension dataset consisting of triples containing question-answer pairs along with distant evidence supporting the answer. Answer may not be directly obtained by span prediction and context is very long.

### Reading comprehension:

11. **RACE** - Large scale reading comprehension dataset. Collected from English examinations designed for middle and high school students. Each example has a long article string, a question and 4 possible answer choices. System is required to identify the right answer among the 4 given choices.
12. **SQuAD** - Standford Question Answering Dataset. Consists of questions by crowdworkers on Wikipedia articles. Ansswer is either a span of text from reading passage or is unanswerable. Each example has context text, question, and answer span. Dataset size - 87599 train and 10570 val examples.

### Mathematial Reasoning:

13. **MATH** - Highschool mathematics problems written in LaTeX. 
14. **GSM8K** - Diverse school-level math word problems taking between 2 to 8 steps to solve involving elementary arithmatics operations. Each example consists of a question string and solution string containing multiple steps of reasoning with calculator annotations. Dataset size - 8.5K examples (Train-7.5K, Test-1K)

### Code Generation:

15. **HumanEval** - Includes programming problems to test the LLMs on code generations. Each example consists of a prompt (includes function header, docstring and a few examples), solution for the prompt, function to test the generated code for correctness and entry point for test. Dataset has 164 rows. GPT-4 based model leads the leaderboard followed by GPT-3.5 based approach.
16. **MBPP** - Crowdsourced python programming problems covering fundamentals. Each example has a task description, code solution and 3 test cases. Size - around 100 examples.

### Multitask Language Understanding

17. **MMLU** - Massive Multitask Language Understanding.Benchmark designed to evaluate LLMs on multiple choice questions from different domains (STEM, Humanities, Social Sciences and Other) in zero/few shot settings. Chinchilla-70B leads the official leaderboard followed by Gopher.

### Multi-hop QA:

18. **HotPotQA** - Each question requires reasoning on mulitple Wikipedia passages. Each example has a question string, context (multiple Wikipedia passages), level of question (easy, medium or Hard), answer, question type, supporting facts locations in the context (required for reasoning allowing strong supervision and explainable predictions). Data Size - 113K QA pairs.

### Fact Verification:

19. **FEVER** - Fact Extraction and VERification. Contains claims by modifying the senteces from wikipedia. Each example consists of claim, label (Supported, Refuted or NotEnoughInfo), evidence within the Wikipedia passage for the label. Data has 185,445 manually verified claims.

### Language Modeling:

20. **Penn Treebank (PTB)** - Consists of articles from Wall Stree Jounal, where each token is labelled with it's Part of Speech Tag. Dataset contains 38219 sentences and 912344 tokens. 
21. **LAMBADA** - Aims to capture long range context. System is asked to predict the last word of a sentence after reading a long context.

### Other Tranditional Language Understanding Benchmarks:

22. **GLUE Bechmark** - General Language Understading Evaluation. Collection of 9 different datasets (CoLA, Stanford Sentiment Treebank (SST), Microsoft Research Paragraph Corpus (MRPC), Semantic Textual Similarity (STS), Quora Question Pairs (QQP), Multi-Genre NLI (MNLI), Questions NLI (QNLI), Recognizing Textual Entailment (RTE), Winograd NLI (WNLI)), formulated mostly as sentence or sentece-pair classification.
