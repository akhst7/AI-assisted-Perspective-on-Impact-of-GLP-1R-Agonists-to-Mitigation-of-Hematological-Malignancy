<img width="690" height="690" alt="under-construction-sign-design-template-70502891e7dc676869296d8e513f4f7d_screen" src="https://github.com/user-attachments/assets/e84206c4-fd80-4e51-af9a-2e12d3bea907" />

# AI-assisted-Perspective-on-Impact-of-GLP-1R-Agonists-to-Mitigation-of-Hematological-Malignancy 

My perspectives on whether GLP-1R Agonists, known for weight control may have unexpected impact in mitigating progressions of mutation driven clonal hematopoiesis  into hematological malignancy.
I was going to write this article for **Medium** but did not go as I planned.  Initially, I heavily let LLM to research relevant information (basically literature search) and create a draft. I was planning to edit the draft and publish.  LLMs I used had kept making errors and did not like the casual writing styles proposed by LLMs.  So I decided to let LLMs do research and write a draft for peer-reviewed journals with more strict rules, and then All of sudden, it stop making as many errors.  As suggested by many, feeding LLMs more detailed information would make them more focus on the subject and they will proceed with less hallucination.  

The models and agents that I have been playing with are;

| Model | Agent |
| :---: | :---: |
| Jundot/Qwen3.6-35B-A3B-oQ4e-mt | Omlx | 
| Jundot/DeepSeek-V4-Flash-0731-oQ2.5e | Omlx |
| Youssofal/Qwen3.8-27B-MTPLX-Optimized-Quality-FP16 | MTPLX |
| Youssofal/Qwen3.8-Flash-Next-MTPLX-Optimized-Speed | MTPLX + OpenWeb UI |
| unsloth/Qwen3.5-4B-MTP-GGUF | Unsloth |
| unsloth/Qwen3.8-27B-GGUF | Unsloth |
| bartowski/Qwen3.8-27B-GGUF | Unsloth |
| Rednalreden/DeepSeek-V4-Flash-0731-dwarfstar-q2-gguf | Unsloth |
| unsloth/Qwen3.8-Flash-Next-GGUF | Unsloth |
| incoai/Qwen3.8-27B-Splash | Splash-M1 + OpenWeb UI |
| Qwen3.8-Flash-Next-Q4.gguf | dstar4-M1 + OpenWeb UI |

My system;
MacStudio with 128GB RAM and M1 Ultra (64 core GPU) 
Interestingly, M1 GPU does natively support (hardware support) fp16 but not bf16 but it can still run bf16 models (e.g. Gemma and Qwen) through fallback MacOS emulation though suffers from significant slow down. Bf16 is hardware supported from M2 on.  According to the recent reviews, M5 and M6 GPUs are truly optimized for the LLM use.  

I will not discuss pros and cons of each of these model+agent, except that I started using Omlx and Qwen3.5 model and ended up with **Splas-M1** and **Dstar4-M1** with those Qwen3.8 models respectively.  Splash-M1 was ported from **Inco's Splash** (https://github.com/incoai/splash) and Dstar4 was forked from **antirez/ds4 (DwarfStar)** (https://github.com/antirez/ds4) by Erik Paperniuk (https://github.com/paperniuk).   

To make the story short, I started using Omlx with Qwen, Gemma, or Deepseek but then I switched to MTPLX when Qwen3.8 arrived because of the significant speed gain (ave 15 vs 25 token/s) without compromising the quality of chat/discussion.  I use OpenWeb UI for the chat interaction.  OpenWeb UI has a few advantage over the internal web chat interface by Omlx and MTPLX, for example, an ability for OpenWeb UI to use the integrated tools which are essentially identical to MCPs.  The integrated tool is basically a python script written for connecting external resources through their APIs.  Another significant reason is that OpenWeb UI is equipped with an internal terminal called **OpenTerminal** which works just like the terminal, allowing the LLM agent to run command lines and access beyond its sandboxed directory in the confined memory space.  Unsloth can do this also but having the terminal access can provide more advantages in my opinion.  

Anyways, as I was learning more by reading **Reddit posts** regarding LLMs, AI agents and interfaces, I noticed that almost every discussion had obsessively focused on how fast (token per sec) newer models can be run.  I was not really concerned about how fast my LLM setup can complete the task but a quality of output.  My tasks are heavy on inference 
