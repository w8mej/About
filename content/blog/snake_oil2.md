---
title: "Part 2: The Glittery AI Magicians with a Probability Problem"
date: 2024-03-15T11:00:37.434Z
extra:
  featured: true
  link: https://builtin.com/artificial-intelligence/artificial-intelligence-cybersecurity
  bibtex: /media/nltp.bib
  pubtype: Article
  image: /media/aisnakeoil.png

description: "Part 2 diving into the hype, we unravel the truth behind startups using AI as their secret sauce. Autoregressive LMs like ChatGPT might dazzle, but when the glitter settles, the limitations—especially in infosec—reveal a gamble where the stakes are sky-high and the odds, well, exponential."
taxonomies:
  tags:
    - Autoregressive model critique
    - Error propagation in AI
    - AI reliability challenges
    - Infosec and AI limitations
    - AI error detection
    - Model training complexities
    - AI design considerations
    - Exponential error rates
    - AI in cybersecurity flaws
    - Context-aware AI development


---
I am going to focus on a few startups where they blatantly or indirectly blatantly demonstrate they utilize autoregressive language models as their magic sauce to provide value.  Unfortunately, there are fundamental challenges associated with autoregressive language models (LMs such as ChatGPT, Claude, Code Llama, etc..), which generate text one token (e.g., a word or a piece of a word) at a time, based on the sequence of tokens that came before. FYI this process is what makes them "autoregressive": each new token is generated with regard to the previously generated sequence, attempting to predict the next most likely token given the context.

But why is this a problem when best effort may be acceptable for many infosec program needs and workloads? Let’s break up that probability model into its’ distinct components because it is more than just playing the odds.

### **Autoregressive Prediction and Error Propagation**

1. **Autoregressive Prediction:** In the context of language models, generating text involves predicting the next token based on the preceding ones. For example, given the start of a sentence, the model predicts the next word, then the next, and so on, with each prediction based on the cumulative context provided by all previously generated tokens.
2. **Probability of Error per Token:** For any given token, there's a certain probability that the model will generate a token that does not align with a coherent or factually correct continuation of the text. This could be due to the vast number of possible continuations, limitations in the model's understanding, or ambiguities in the input text.
3. **Error Independence Assumption:** There is a very strong assumption that the probability of errors is independent across each token generated. This means that the chance of making a mistake at any step does not influence or depend on the chance of making a mistake at another step. While this assumption simplifies the understanding of error propagation, real-world dependencies (contextual clues, syntactic structures, etc.) mean errors are not always independent.  Especially when dealing with information security, production, engineering operations, SRE, technology stacks, vulnerability remediation, and/or tailored knowledge base services.  For instance, the decision to disable writable permissions to a S3 bucket that is made available to a different AWS account ID is failure when the context of that “oops” is the AWS account id’s ownership by your banking partner.  Or they use said id to drop ACH files in your account for processing results.
4. **Exponential Decrease in Correctness Probability:** Given this assumption of error independence, as the model generates more tokens, the likelihood of staying entirely within a "correct" or reasonable path of generation decreases exponentially. With each token generated, there's a chance of veering off into less accurate, less relevant, or completely nonsensical text. The impact of errors compounds because each new token relies on the context set by all previous ones, including any errors.

Remember, we are not talking about linear rates, but exponential

![LinearExpo](/media/linexpo.png)

### **Implications for Language Models**

- **Error Accumulation: The compounding nature of errors means that longer texts are more likely to contain inaccuracies or incoherencies. This is particularly relevant for complex or nuanced topics where precision is crucial.**
- **Quality Control Challenges:** Ensuring the reliability of output from autoregressive LMs becomes increasingly difficult as the text lengthens. This necessitates sophisticated mechanisms for error detection and correction, which are active areas of research.

![AiIsHumans](/media/gptsecretishumans.png)

- <https://www.nytimes.com/2023/09/25/technology/chatgpt-rlhf-human-tutors.html>
- **Design Considerations for AI Systems:** Understanding the nature of error propagation in autoregressive models is critical for designing better AI systems. Creators and consumers must account for the exponential increase in error probability, perhaps by incorporating corrective feedback loops, utilizing more context-aware generation strategies, or developing models that can better handle the dependencies and nuances of language.  More on these points below as this is an extremely active area of theoretical mathematical, applied mathematical, and informatics research.

### [Continued in Part 3 of 9](../snake-oil3/)
