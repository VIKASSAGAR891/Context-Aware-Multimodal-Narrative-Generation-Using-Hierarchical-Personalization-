# Context-Aware Multimodal Narrative Generation System

## Overview

This project presents a context-aware multimodal narrative generation system that integrates structured user demographics and visual scene descriptions into a large language model to produce personalized stories.

Unlike traditional prompt-based generation, this system introduces hierarchical conditioning, where different contextual signals influence distinct aspects of narrative generation. The system is designed not only for generation but also for quantitative evaluation of personalization effects.

This work was developed as part of a major project and extended into a complete experimental pipeline.

---

## Problem Statement

Modern generative systems produce fluent text but lack structured personalization and controlled multimodal integration. Existing approaches either:

- Use generic prompts without user adaptation  
- Apply shallow personalization without measurable evaluation  
- Treat multimodal inputs without understanding their hierarchical influence  

This project addresses these limitations by designing a system that:

- Integrates user and visual context in a structured manner  
- Controls emotional and descriptive aspects separately  
- Evaluates outputs using quantitative linguistic metrics  

---

## System Architecture

The system follows a four-stage pipeline:

1. Input Acquisition  
   - User Profile (age, interest, tone)  
   - Visual Scene Description (bright or dark environment)

2. Hierarchical Context Integration  
   - Demographic context influences emotional tone  
   - Visual context influences environmental description  

3. Narrative Generation  
   - Structured prompt construction  
   - LLM-based story generation  

4. Quantitative Evaluation  
   - Lexical Diversity (Type-Token Ratio)  
   - Sentence Length  
   - Sentiment Polarity  
   - Shannon Entropy  

---

## Key Concepts

### Context-Aware Generation
The system adapts output based on structured user attributes rather than generic prompts.

### Multimodal Conditioning
Visual scene descriptions are integrated alongside user context to influence narrative structure.

### Hierarchical Conditioning
Different inputs affect different dimensions:
- User profile → emotional tone  
- Visual context → descriptive vocabulary  

---

## Experimental Design

Three configurations were evaluated:

1. Baseline  
   - No personalization  
   - Neutral narrative generation  

2. Child Profile  
   - Age: 10  
   - Tone: positive and simple  
   - Interest: magical storytelling  

3. Adult Profile  
   - Age: 25  
   - Tone: dark and suspenseful  
   - Interest: dark fantasy  

Each configuration was evaluated over multiple runs to ensure statistical consistency.

---

## Evaluation Metrics

### Lexical Diversity (Type-Token Ratio)
Measures vocabulary richness.

### Sentence Length
Indicates structural complexity.

### Sentiment Polarity
Measures emotional tone (-1 to +1).

### Shannon Entropy
Measures distribution and diversity of word usage.

---

## Results Summary

- Lexical diversity increases with personalization  
- Adult narratives show higher linguistic complexity  
- Child narratives maintain simpler structure  
- Sentiment varies significantly based on user profile  
- Identical visual inputs produce different emotional outputs depending on demographic context  

These findings validate the effectiveness of hierarchical conditioning.

---

## Multimodal Analysis

Additional experiments were conducted using visual context:

- Bright scene → positive descriptive vocabulary  
- Dark scene → atmospheric and shadow-based vocabulary  

Key observation:

The same dark visual scene produced:
- Positive narratives for child profiles  
- Negative narratives for adult profiles  

This demonstrates controlled emotional modulation through hierarchical context integration.

---

## Implementation Details

- Language Model: llama-3.3-70b-versatile  
- API Integration: Groq  
- Programming Language: Python  
- Libraries:
  - NumPy  
  - Matplotlib  
  - TextBlob  

---


## Key Contributions

- Designed a context-aware multimodal generation framework  
- Implemented hierarchical conditioning for structured personalization  
- Developed a quantitative evaluation pipeline for narrative analysis  
- Demonstrated measurable differences in emotional and linguistic outputs  
- Built a modular and reproducible experimental system  

---

## Limitations

- Visual input is text-based, not true image embeddings  
- Limited user attributes  
- No human evaluation studies  
- Dependence on a single LLM  

---

## Future Work

- Integration with vision-language models (CLIP, multimodal transformers)  
- Expansion of user context (memory, preferences, history)  
- Real-time interactive system deployment  
- Human-in-the-loop evaluation  

---

## Conclusion

This project demonstrates that structured contextual conditioning enables controlled, measurable, and interpretable personalization in narrative generation systems. The results highlight the importance of separating emotional and descriptive influences in multimodal AI systems.

---

## Author

Vikas Narlakanti  


---

## License
This project is provided for academic and research purposes only.

Parts of this work are based on a published research paper. Due to potential copyright and publication policies, this repository is intended strictly for educational demonstration and non-commercial use.
