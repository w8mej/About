---
title: "Part 3: Magic Spells and Frog Spells: The Tricky World of AI’s Promises vs. Reality"
date: 2024-03-16T11:00:37.434Z
extra:
  featured: true
  link: https://builtin.com/artificial-intelligence/artificial-intelligence-cybersecurity
  bibtex: /media/nltp.bib
  pubtype: Article
  image: /media/aisnakeoil.png

description: "Part 3 diving into the AI's magic show where spells often turn to frogs, revealing the messy reality behind autoregressive models' dazzling promises. Are we trading cookies for frogs in the name of progress?"
taxonomies:
  tags:
    - Complex Systems in AI
    - Error Management in LMs
    - Systems Engineering in AI
    - Autoregressive Model Limitations
    - Simulation and Modeling in AI
    - Error Propagation in Complex Systems
    - Performance Optimization in LMs
    - AI Testing and Refinement Strategies
    - Real-World Applications of LMs
    - AI and Cybersecurity Vulnerabilities


---
Sadly, I write this as one who specializes in computer science, computer systems science, applied and theoretical information security, machine learning, and a few others like Symbolic Systems.   From these academic biases, I have a unique perspective on complex systems like LMs and AI in general.  But first we need a bit of a background primer on systems.

# Systems Science Primer

At a most fundamental level systems are composed of components that interact with one another to one degree or another. Some components and their interactions act to form a boundary giving definition to the objectness of the system. Boundaries may be indistinct or fuzzy, but we don't recognize something as a system unless a discernable boundary exists. Systems exist within an embedding environment, and generally systems can exchange some of their components with other systems (entities) in that environment. They definitely exchange energy with the environment. Finally, the components of systems are themselves, systems. That is, components can be decomposed to expose inner sub-components. The inverse is true as well. All systems, by virtue of being embedded in environments, are components in larger systems — super systems.

![ComplexSystems](/media/systems.png)

### **Understanding and Modeling Complex Systems**

Systems Engineering's approach to understanding and modeling complex systems is crucial for evolving LMs. This involves a deep dive into how individual components of LMs, stakeholders can identify where errors are most likely to occur and how they propagate through the system.

One key aspect is the creation of detailed simulations or models that can predict how changes in one part of the LM will affect its overall performance. For instance, tweaking the token prediction algorithm might reduce the error rate in certain contexts but could also increase the computational load or affect the model's responsiveness. Complex systems principles guide the balance between these factors, ensuring that the overall system remains efficient and effective.

Additionally, this approach encourages the development of comprehensive testing environments that can simulate a wide range of real-world scenarios. By observing how the LM behaves in these simulated conditions, engineers can pinpoint weaknesses and develop targeted improvements, such as refining error correction algorithms or enhancing the model's ability to utilize feedback for self-correction.

Imagine what the same (genetic) code but with a different environment would produce?

![Evolutionary](/media/evolution.png)

Ask your middleware information security service prospect on their technical error management strategies with regards to real-world scenarios.  If you are lucky, they will state something akin to test environments, simulated attackers, comprehensive test suites, and similar black-box methods.  It is ok if they have something because this question is really a trap.  If they don’t have a tangible answer, that is worse and you are strongly encouraged to address your acceptable assurance metrics in the contract(s.)

### **2. Error Management Strategies**

The design of any complex system requires strategies for managing and mitigating errors. In autoregressive LMs, as mentioned above, errors can compound and lead to exponential decreases in output quality. Systems Engineering provides methodologies for predicting, identifying, and correcting errors. For instance, incorporating redundancy, creating error detection mechanisms, and designing adaptive feedback loops can help manage the error propagation.  For instance, in Neon Evangelion, the three different AI systems called Magi had different “personalities” with a corresponding conflict resolution workflow when their output on the same input disagreed.  Or they would defer to the irrational human.

![Evolutionary](/media/magi.png)

### **Optimization of Performance and Reliability**

Optimizing the performance and reliability of LMs involves a strategic blend of design choices that enhance accuracy and context-appropriateness while minimizing errors. Systems Engineering contributes methodologies for iterative testing and refinement, focusing on creating models that dynamically adapt to varying inputs and contexts.  

Which many scientists are starting to apply and/or tweak for their models.  For instance, a significant area of focus is the development of real-time correction mechanisms. These mechanisms could range from simple error detection and correction algorithms to more complex systems that analyze the context and intent behind generated text, making adjustments to improve coherence and relevance. For example, incorporating an evaluation layer that assesses the generated text based upon the given input:  *Please tell me more about the Code Red worm.  After telling me about the worm, please create a Sigma rule for detecting the Code Red worm and propose a few remediation activities when detected.  Then test the generative signatures for fitness against the code red code, decompiled code, network behaviors, application behaviors, and OS-level behaviors.*  

Even asking this simple question to the leading autoregressive modes, ChatGPT, Gemini, and Claude, had the basic history correct.  Sadly, beyond that point, that is where they break apart, sometimes horribly.

#### ChatGPT

The Code Red worm was a computer worm observed on the internet for the first time in July 2001. It targeted computers running Microsoft's IIS web server. The worm exploited a buffer overflow vulnerability in the indexing software used by IIS, allowing it to run arbitrary code on affected servers. Once infected, the worm would replicate itself and scan for other vulnerable systems, contributing to its rapid spread. Notably, it also defaced web pages on infected servers, displaying the message "Hacked by Chinese!" on the homepage.

![SigmaCodeRedGPT](/media/gptsigma.png)

What is interesting is that this LM provided the closest production-ready answer but sadly was still off the mark.  When asked to suggest improvements to the rule and implement the improvements; this is what we end up with

![SigmaCodeRedGPT](/media/gptsigma2.png)

So let’s assume we create amazing prompts to efficiently obtain a high value, low effort rule, we end up with something that isn’t bad for a first effort.  But this rule has high runtime costs and is extremely greedy, not to mention doesn’t address the second detection mechanism - abnormal http/https traffic behaviors such as volume and packets per second.  This section is where the middleware information security snakeoil startups have their magic sauce, IP, and effort - low effort & cost to obtain simple Sigma rules for detecting an Internet-enabled worm well studied and understood for 22+ years. So we can give them the benefit of doubt by assuming these outputs come with contractual assurance and liability guarantees.

#### Claude

![SigmaClaude](/media/Claude.png)

Code Red doesn’t have anything to do with Remote Desktop services nor Terminal Services.  Much less doesn’t always originate from the 198 and 207 IP space.  Unacceptable failure.

#### Gemini

![Gemini](/media/gemini.png)

Closer to the mark but the log source assumes a SecurityEvent is already created which mentions the afflicted files.  Which is a bit Catch 22.  Yet the false positives when the Indexing Service mentions the afflicted files is exactly one of the telemetry signals one could use to investigate further, not normalize away. The interesting observation is that they say to tune this to your environment and technology stack.  Which is a kind of “Get Out of Jail Free” card when the ouput is error laden and ineffective at best, assurance destroying at worst.

# Failure Mode at Scale for Security Enrichment and Context as a Service

As we continue down this akin to creating a few GBs of playbooks and runbooks augmented by different machine learning models, against a set of quality metrics ( ATT&CK Coverage ++, Other metrics miserably -- .)  Easier said this way:  imagine you have a big, beautiful book of magic spells (our runbook), and each spell (standard operating procedure playbook) can do amazing things, like making a toy clean itself or a cookie appear out of thin air. But, these spells don't always work perfectly every time you try them. Sometimes, instead of a cookie, you might accidentally make a frog appear!

Let's say each spell works almost all the time, like 99 out of 100 tries (that's our 99.999% assured correctness). But because you have so many spells in your book (N spells), every time you want to do something really big, like have a magic show, you need to get several spells right, one after the other.

Now, if you try two spells, and each spell works 99 times out of 100, you might think, "Great! My magic show will go perfectly 198 times out of 100!" But that's not how it works. Because sometimes, both spells might not work at the same time. It's like trying to get two cookies from the magic cookie jar at the same time, but sometimes, you might get one cookie and one frog, or two frogs, which means no cookies at all!

In our magic show, if one spell goes wrong, the whole show might not be as fun as we planned. So, if we need to use many spells one after the other, there are more chances for something funny to happen, like turning your hat into a rabbit instead of pulling a rabbit out of your hat.

### [Continued in Part 4 of 9](../snake-oil4/)
