---
title: "Part 5: Breaking AI's Chains: Beyond Fine-Tuning into Chaos"
date: 2024-03-18T11:00:37.434Z
extra:
  featured: true
  link: https://builtin.com/artificial-intelligence/artificial-intelligence-cybersecurity
  bibtex: /media/nltp.bib
  pubtype: Article
  image: /media/aisnakeoil.png

description: "Part 5 fine-tuning AI is like teaching a parrot literature; expect poetry about birds! Delve into the chaos where models trip over reality's unpredictability. Is AI's future just a series of well-meaning stumbles?"
taxonomies:
  tags:
    - Fine-Tuning Limitations
    - AI Model Sensitivity
    - Robust AI Generalization
    - Error Correction in AI
    - Training Data Diversity
    - AI Interpretability
    - Computer Systems Science Research
    - AI in Cybersecurity
    - Chaos Theory and AI
    - Next-Gen AI Challenges

---
### **Fine-tuning and Its Limits**

Fine-tuning the model on a wide array of questions is a limited strategy to improve performance. Fine-tuning involves adjusting a pre-trained model's parameters slightly to better fit a specific task or domain such as vulnerability remediation or incident response agent reasoning. While effective to an extent, fine-tuning cannot overcome the inherent limitations posed by the curse of dimensionality. The diversity and complexity of potential inputs mean that it's practically impossible to cover all bases, leading to situations where the model may generate nonsensical or wildly inaccurate responses to unexpected prompts.  For instance, a base LM trained on birds and supervised training on literature will result in birds in literature, literally.

![TuningBirds](/media/finetuned.png)

### **Understanding Prompts and Model Limitations**

Even small changes or the introduction of elements not seen during training (like mixing languages) can "jailbreak" the model, causing it to produce irrelevant or incorrect outputs. This underscores the sensitivity of LLMs to their input and the difficulty in creating models that can robustly handle a wide range of inputs without error.  IE how do they handle the Butterfly effect made mainstream popular by Jeff Goldblum?  

![ChaosTheory](/media/chaostheory.png)

### **Implications for Computer Systems Science**

Which is why we see VERY active research that hope to deliver results over the next decade in the following areas;

- **Robustness and Generalization:** Developing techniques that enhance the model's ability to generalize from its training data to a broader array of real-world inputs.  At the forefront of our inquiry lies the pursuit of robustness and generalization in AI systems. The goal here is to create models that are not only adept at learning from their training data but are also capable of applying this knowledge across a spectrum of real-world scenarios. Such systems are akin to scholars who, having mastered the principles of their disciplines, can apply their wisdom universally.
- **Error Handling and Correction:** Implementing more sophisticated mechanisms for detecting when the model is likely to produce an error and correcting course in real-time.  Navigating the digital realm requires a nuanced approach to error handling and correction. It's about creating systems that, aware of their limitations, can dynamically adapt and correct their course. This level of self-awareness and adaptability is crucial for developing AI that can reliably function in the unpredictable landscape of cybersecurity threats.
- **Training Data Diversity:** Continuously expanding and diversifying the training datasets to better represent the vast space of potential prompts and responses.  A foundational element of our work involves enriching AI with diverse training data. This diversity ensures that our systems have a broad and inclusive understanding of the digital world, akin to a well-traveled global citizen. Such systems are better equipped to recognize and adapt to the multifaceted nature of cybersecurity challenges, drawing from a rich tapestry of scenarios and experiences.
- **Interpretable Models:** Working towards models that can explain their reasoning or the basis for their outputs, which could help identify and mitigate errors before they occur.  Transparency and interpretability in AI models are essential. They allow us to understand the 'how' and 'why' behind AI decisions, providing insights that are critical for trust and reliability in cybersecurity applications. This pursuit of clarity and openness is fundamental to our collective efforts to advance the field.

### [Continued in Part 6 of 9](../snake-oil6/)
