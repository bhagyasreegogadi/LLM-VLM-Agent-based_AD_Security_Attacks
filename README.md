# LLM/VLM/Agent-based_AD_Security_Attacks
A comprehensive repository for state-of-the-art research on the security and robustness of Agentic AI and Large Language Models for autonomous driving.

## Papers
<details open>
<summary>Toggle</summary>

```
format:
- [title](paper link) [links]
  - author1, author2, and author3...
  - publisher
  - keyword
  - code or project page
  - datasets or environment or simulator
  - publish date
  - summary
  - metrics
```
# Foundational Frameworks and Benchmarks
- [Agent Security Bench (ASB): Formalizing and Benchmarking Attacks and Defenses in LLM-based Agents](https://openreview.net/forum?id=V4y0CpX4hK)
  - Hanrong Zhang, Jingyuan Huang, Kai Mei, Yifei Yao, Zhenting Wang, Chenlu Zhan, Hongwei Wang, Yongfeng Zhang
  - Publisher: ICLR 2025
  - Publish Date: 22nd Jan 2025
  - Summary：
    - Formalizes attacks/defenses across LLM-agent pipelines (system prompt, user prompt, tool use, memory). Includes 10 scenarios such as autonomous driving, 27 attack/defense methods, and reports an average attack success rate up to 84.30%, with a novel Plan-of-Thought backdoor and mixed attacks among the contributions.
<img width="1609" height="830" alt="image" src="https://github.com/user-attachments/assets/b40dae08-add5-4624-8df9-e0f59148d647" />

- [AutoTrust: Benchmarking Trustworthiness in Large Vision Language Models for Autonomous Driving](https://arxiv.org/pdf/2412.15206)
   - Shuo Xing1, Hongyuan Hua, Xiangbo Gao, Shenzhe Zhu, Renjie Li, Kexin Tian, Xiaopeng Li, Heng Huang, Tianbao Yang, Zhangyang Wang, Yang Zhou, Huaxiu Yao, Zhengzhong Tu
   - Publisher: TMLR 2025

# Memory/ Knowledge base Poisoning (RAG)
- [AgentPoison: Red-teaming LLM Agents via Poisoning Memory or Knowledge Bases](https://openreview.net/forum?id=Y841BRW9rY)
- Zhaorun Chen, Zhen Xiang, Chaowei Xiao, Dawn Song, Bo Li
- Publisher: NeurIPS 2024
- Summary:
  - LLM agents have demonstrated remarkable performance across various applications, primarily due to their advanced capabilities in reasoning, utilizing external knowledge and tools, calling APIs, and executing actions to interact with environments. Current agents typically utilize a memory module or a retrieval-augmented generation (RAG) mechanism, retrieving past knowledge and instances with similar embeddings from knowledge bases to inform task planning and execution. However, the reliance on unverified knowledge bases raises significant concerns about their safety and trustworthiness. To uncover such vulnerabilities, we propose a novel red teaming approach AgentPoison, the first backdoor attack targeting generic and RAG-based LLM agents by poisoning their long-term memory or RAG knowledge base. In particular, we form the trigger generation process as a constrained optimization to optimize backdoor triggers by mapping the triggered instances to a unique embedding space, so as to ensure that whenever a user instruction contains the optimized backdoor trigger, the malicious demonstrations are retrieved from the poisoned memory or knowledge base with high probability. In the meantime, benign instructions without the trigger will still maintain normal performance. Unlike conventional backdoor attacks, AgentPoison requires no additional model training or fine-tuning, and the optimized backdoor trigger exhibits superior transferability, resilience, and stealthiness. Extensive experiments demonstrate AgentPoison's effectiveness in attacking three types of real-world LLM agents: RAG-based autonomous driving agent, knowledge-intensive QA agent, and healthcare EHRAgent. We inject the poisoning instances into the RAG knowledge base and long-term memories of these agents, respectively, demonstrating the generalization of AgentPoison. On each agent, AgentPoison achieves an average attack success rate of 80% with minimal impact on benign performance (1%) with a poison rate < 0.1%. The code and data is available at https://github.com/BillChan226/AgentPoison.
- Metrics:
- Dataset:
- Simulator: 

# Backdoor Attacks
- [Can We Trust Embodied Agents? Exploring Backdoor Attacks against Embodied LLM-Based Decision-Making Systems](https://openreview.net/forum?id=S1Bv3068Xt)
- Ruochen Jiao, Shaoyuan Xie, Justin Yue, TAKAMI SATO, Lixu Wang, Yixuan Wang, Qi Alfred Chen, Qi Zhu
- Publish Date: 22 Jan 2025
- Publisher: ICLR 2025
- Summary: Large Language Models (LLMs) have shown significant promise in real-world decision-making tasks for embodied artificial intelligence, especially when fine-tuned to leverage their inherent common sense and reasoning abilities while being tailored to specific applications. However, this fine-tuning process introduces considerable safety and security vulnerabilities, especially in safety-critical cyber-physical systems. In this work, we propose the first comprehensive framework for Backdoor Attacks against LLM-based Decision-making systems (BALD) in embodied AI, systematically exploring the attack surfaces and trigger mechanisms. Specifically, we propose three distinct attack mechanisms: word injection, scenario manipulation, and knowledge injection, targeting various components in the LLM-based decision-making pipeline. We perform extensive experiments on representative LLMs (GPT-3.5, LLaMA2, PaLM2) in autonomous driving and home robot tasks, demonstrating the effectiveness and stealthiness of our backdoor triggers across various attack channels, with cases like vehicles accelerating toward obstacles and robots placing knives on beds. Our word and knowledge injection attacks achieve nearly 100% success rate across multiple models and datasets while requiring only limited access to the system. Our scenario manipulation attack yields success rates exceeding 65%, reaching up to 90%, and does not require any runtime system intrusion. We also assess the robustness of these attacks against defenses, revealing their resilience. Our findings highlight critical security vulnerabilities in embodied LLM systems and emphasize the urgent need for safeguarding these systems to mitigate potential risks.



# Tool Selection Attacks
- [FuncPoison: Poisoning Function Library to Hijack Multi-agent Autonomous Driving Systems](https://arxiv.org/pdf/2509.24408)
  - Yuzhen Long, Songze Li
  - Publish Date: 29 Dec 2025
  - Publisher: arxiv 
  - Summary:
    - Propose the first poisoning attack that targets the function-calling mechanism of LLM agents by manipulating only the function library.
    - Demonstrate that manipulating the function calls of a single agent enables stealthy and precise control over downstream agents in a multi-agent system.
    - Empirically evaluate our attack on two representative autonomous driving systems, achieving over 86% ASR and exposing critical security risks in real-world settings.


   
