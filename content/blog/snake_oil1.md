---
title: "Part 1: Thoughts on the Cyber AI Hustle"
date: 2024-02-22T11:00:37.434Z
extra:
  featured: true
  link: https://builtin.com/artificial-intelligence/artificial-intelligence-cybersecurity
  bibtex: /media/nltp.bib
  pubtype: Article
  image: /media/aisnakeoil.png

description: "Part 1 of a series diving into AI's cybersecurity hype, I reveal how LLMs promise much yet often deliver generic fixes that miss the mark. My critique explores the gap between AI's allure and its actual utility, urging a balanced approach that combines AI's power with human insight."
taxonomies:
  tags:
    - AI cybersecurity critique
    - LLM limitations
    - Middleware security solutions
    - Generic remediation pitfalls
    - Cybersecurity program metrics
    - Hybrid AI-human oversight
    - Anomaly detection algorithms
    - Continuous training data updates
    - AI in threat intelligence
    - Ensemble learning techniques

---
Over the past few months, I was asked to look into yet another “Llama, ChatGPT, or <insert autoregressive language model of the day HuggingFace featured> as a black box service” middleware company pretending to be yet another security-related engineering knowledge dictionary, orchestration, and/or remediation service.  IE give us your pentest test findings in CSV (delivered by no reputable firm, ever…) and we will produce non-tailored generic content for Engineering and Engineering Operations to quickly reject the pull request that utterly failed to correct the finding for a default tech stack that isn’t applicable to your setup.  For instance, you haven’t patched your CUPS print library so here is a PR to patch it by reving the package version.  Yet the PR is rejected because the library exists on the image but the package isn’t installed nor the CVE mentioned the executable, not library, is affected.  Since the binary isn’t installed, rejected.  Or yet another “Validate Input/Sanitize Output” remediation PR against your Scala code base with the entire Java ESAPI library with Spring’s Java Framework awaiting a merge.  Right…..

The challenge I have with these services is that they rely upon technology and workflows that are not designed nor will achieve the outcomes desired unless equity is the startup investors’ only product.  Where the middleware startup is aligned to cashing out as soon as possible to gullible limited partners while showing traction by having their LPs’ networks purchase said middleware as quick as possible.

![Startup Equity](/media/equityproduct.png)

Looking from the buyer side, it isn’t clear to me the buyers are aware of AI snake oils’ inherent limitations and failures to approach certain business needs.  For instance, when one looks at the remediation and identification of threats, actors, and evil practices; most of the applicable Information Security program metrics will approach and trend towards negative outcomes at best;  

| Metric                        | Description                                                                                                                          | Potential Mitigation                                                                                                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dwell Time**                | Likely to decrease due to continuous automation capabilities of LLMs, albeit with increased error rates from probabilistic methods.  | Implement a hybrid model combining LLM automation with human oversight to verify and correct errors, enhancing accuracy while tensioned against the eventual creation of a look-up table |
| **Mean Time to Acknowledge**  | Could be reduced with LLMs' instant responsiveness, though precision may be variable.                                                | Utilize anomaly detection algorithms alongside LLMs to better identify true positives and reduce false alarms.                                                                           |
| **Mean Time to Detect**       | Speed of detection might improve with LLMs, but accuracy depends on training data quality and understanding of novel threats.        | Continuously update the training data with the latest cybersecurity threats and incorporate feedback loops for learning from false detections.                                           |
| **Mean Time to Contain**      | Unchanged or increased, as LLMs can't fully comprehend nuances of sophisticated cyber threats.                                       | Leverage expert systems in parallel with LLMs for nuanced decision-making in containment strategies.                                                                                     |
| **Mean Time to Recovery**     | Limited improvement due to LLMs' lack of understanding of system interdependencies.                                                  | Integrate LLMs with decision support systems that model system interdependencies to inform recovery strategies.                                                                          |
| **Automation Coverage**       | Expected to expand, yet effectiveness is tempered by varying performance in security scenarios.                                      | Combine LLMs with domain-specific rule-based systems to ensure comprehensive coverage and maintain human oversight.                                                                      |
| **Mean Cost of Pgm Failures** | Costs could rise due to LLMs' misinterpretations and errors in automated decision-making.                                            | Establish a robust monitoring and evaluation framework to quickly identify and correct program failures.                                                                                 |
| **Inadequate Remediation**    | Challenges persist due to LLMs' limitations in generating comprehensive remediation strategies.                                      | Augment LLM recommendations with expert human review to ensure adequacy and completeness of remediation actions.                                                                         |
| **Ghost Remediations**        | May increase, as LLM-driven systems could initiate actions on misinterpreted data.                                                   | Implement strict validation checks before executing remediation actions to ensure they are warranted and effective.                                                                      |
| **Mean Time to Inventory**    | Decreased through faster data processing, yet accuracy might be compromised.                                                         | Supplement LLM analysis with periodic manual audits to verify inventory accuracy and completeness.                                                                                       |
| **ATT&CK Coverage**           | Quicker detection of TTPs could be facilitated by LLMs, but quality and functionality are inconsistent.                              | Integrate LLMs with up-to-date threat intelligence platforms to improve detection quality and functionality.                                                                             |
| **CAPEC Coverage**            | Rapid identification of attack patterns could improve, yet depth and applicability are uncertain.                                    | Enhance LLMs with specialized machine learning models trained specifically on attack pattern recognition to improve depth and applicability.                                             |
| **EPS**                       |                                                                                                                                      | Introduce advanced data normalization and preprocessing techniques to improve LLMs' efficacy in processing event streams.                                                                |
| **Anomalous Safe Rate**       | The rate at which anomalies are safely identified could benefit from LLMs' capabilities, though precision is subject to limitations. | Deploy ensemble learning techniques, combining LLM outputs with those from other anomaly detection systems to improve overall precision.                                                 |

## Approaching but never hitting acceptable cross-over rates

Let's imagine you're texting an incident notification to a friend, one word at a time. Every time you choose a word, there's a tiny chance you might accidentally pick a word that doesn't really fit well into the story. Imagine if every time you send a word, you spin a wheel of fortune that mostly lands on "good word choices" but sometimes lands on "oops, that's a weird word."

Now, let's say you're trying to make sure your whole story makes sense. If you just send a few words, it's pretty easy to keep the story sounding right because you haven't spun that wheel too many times. But, if your story is really long, you're spinning that wheel over and over. Since there's always that small chance of getting a weird word, the more words you send, the higher the chance that at least one of those words will make the story start to sound a bit off. And as you keep going, adding more and more words, these little mistakes can start adding up, making it harder to keep your incident story on track.

These methods how LMs operate are like writing a story. The AI picks one word at a time (like spinning the wheel) to add to the text it's generating. Even if there's just a small chance of picking a word that doesn't quite fit, the longer the text, the more likely it is that the AI will end up including some words or phrases that don't make sense. This problem gets worse pretty quickly as the text gets longer, because the chances of staying perfectly on track go down a lot with each word it adds.  Then before you know it, your friend thinks you are crazy, your reputation ruined, and later are asked to be fired from your role because you lost their trust.

![LM Design](/media/modaldesign.png)

### [Continued in Part 2 of 9](../snake-oil2/)
