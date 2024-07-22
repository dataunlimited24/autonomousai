
# Memo from the CISO

From: Sarah Jung  
To: Alex Hanover  
Subject: Review Generative AI Risk Memo

Hi Alex, can you review the following before I send it out to all? Thanks

---

## Team,

Many of you are very excited to bring the value of generative AI to your teams and products. So are we. GenAI can be deployed with relative ease compared to previous AI technologies, and it holds tremendous potential for our business. At the same time, as with all technologies, there are risks and threats to our business that simply cannot be ignored.

You may have already heard about generative AI risks in the news and other media. In fact, the Open Source Foundation for Application Security (OWASP) has already published a “Top 10 for Large Language Model Applications,” which includes attack vectors like prompt injection, information disclosure, and model theft.

### OWASP Top 10 for Large Language Model Applications
1. **LLM01 - Prompt Injection**
2. **LLM02 - Insecure Output Handling**
3. **LLM03 - Training Data Poisoning**
4. **LLM04 - Model Denial of Service**
5. **LLM05 - Supply Chain Vulnerabilities**
6. **LLM06 - Sensitive Information Disclosure**
7. **LLM07 - Insecure Plugin Design**
8. **LLM08 - Excessive Agency**
9. **LLM09 - Overreliance**
10. **LLM10 - Model Theft**

This is just the beginning. There are new nefarious and adversarial activities emerging all the time. Take the recent example of code hallucination attacks: not unlike the ChatGPT hallucinations you are already familiar with, coding copilots' code can also regularly invent its own components. A coding copilot might provide a code sample with a non-existent library (i.e., a hallucination). This seems harmless until you realize that a clever adversary can create and publish that same library based on knowledge of common code hallucinations. When someone goes to run the code, the adversarial library gets pulled and executed.

Another example involves exploiting the open-source model ecosystems by targeting the emerging model repositories. Some of you may already be experimenting with models and embedding libraries from HuggingFace. You need to know there are two vulnerabilities related to HuggingFace:

1. **The HuggingFace Safetensors Conversion Service Vulnerability**: Allows hackers to send malicious pull requests with attacker-controlled data to any repository on the Hugging Face platform. This enables the hijacking of models submitted through the conversion service. Attackers can extract tokens associated with SFConvertbot to send dangerous pull requests and manipulate models. This poses risks of theft of user tokens, access to datasets and internal models, and widespread supply chain attacks.
2. **The Recently Disclosed LeftoverLocals Vulnerability (CVE-2023-4969)**: Enables retrieval of data from GPGPUs manufactured by Apple, AMD, Qualcomm, and Imagination. This stems from a failure to isolate process memory, allowing local attackers to read memory from various processes, including interactive sessions of other users within an LLM. The result is that sensitive data can be used to [...]

Because this is a new technology, the risks are showing up in new and unexpected ways. As you can see from these examples, they can catch even the most seasoned professionals off-guard.

Overall, we need to ensure everyone is familiar with the risks of this new technology and seek help from your Security and Technology leaders with deploying your Generative AI projects. The major risks associated with Generative AI include data security and privacy risks, where sensitive information could be inadvertently exposed; the potential for generating misleading or false information that can be used nefariously; the possibility of reinforcing existing biases in data, leading to unfair outcomes; and operational and financial risks, such as disruptions or financial losses caused by unmanaged AI systems. Understanding these risks is crucial for ensuring we use AI responsibly.

To ensure we all benefit safely from these powerful tools, please work closely with our Security and IT teams whenever you plan to use generative AI. We will introduce a program for reviewing your generative AI plans to help you mitigate these risks. In addition, we will be offering training sessions to help everyone understand best practices and the importance of secure data handling. By staying vigilant and following our guidelines, we can enjoy the advantages of AI while keeping our organization safe and responsible.

Thank you for your cooperation and dedication to our success.

Warm regards,  
Sarah Jung  
Chief Information Security Officer


