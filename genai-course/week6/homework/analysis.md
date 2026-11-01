Part I: Winning Variation

I found the V5 hybrid to be the best bang for the buck. While I preferred CoT, being a novice and therefore benefiting from step-by-step explanation, it was almost twice the cost.


Part II: Failure Analysis Memo: Conflicting Constraints Reoccurring Failure Mode

One pattern I see relates to the fundamental architectural limitation of an LLM as a probabilistic system lacking ground-truth—it can produce persuasive and plausible methodological critiques while fundamentally misunderstanding the real-world research design that it is evaluating. Another pattern is a simple failure to follow prompt instructions, which even if locally rare could be unacceptably frequent at scale. 

These patterns were most clearly demonstrated with the “conflicting constraints” class of adversarial input, which my best prompt struggled with even after repair. Specifically, (1) the model produced locally plausible statements without cross-checking them against each other for real-world feasibility, such as recommending data-labeling in clear constraint violation; and (2) did not double-check constraint pairs as prompted prior to output, such as a one-week completion timeframe. 

This tells me that prompt engineering can mitigate but likely never eliminate fundamental LLM architectural limitations of a merely probabilistic rather than ground-truth understanding of reality. Prompts may also be partially ignored some of the time, which a schema may not catch if the output is formatted correctly. System-level solutions are likely required to mitigate these failure modes, such as a larger model, or a second verification pass. 
