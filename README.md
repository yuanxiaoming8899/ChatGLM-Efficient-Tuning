<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGLM 高效调优</font></font></h1><a id="user-content-chatglm-efficient-tuning" class="anchor" aria-label="永久链接：ChatGLM 高效调优" href="#chatglm-efficient-tuning"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a href="https://github.com/hiyouga/ChatGLM-Efficient-Tuning/stargazers"><img src="https://camo.githubusercontent.com/6c5cacd063e1c56b970d6184dcdf39022d1601988062e3ed2f4c69e2fea64c19/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f6869796f7567612f43686174474c4d2d456666696369656e742d54756e696e673f7374796c653d736f6369616c" alt="GitHub 存储库星星" data-canonical-src="https://img.shields.io/github/stars/hiyouga/ChatGLM-Efficient-Tuning?style=social" style="max-width: 100%;"></a>
<a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/LICENSE"><img src="https://camo.githubusercontent.com/40db6e6582eef962a98c4a41a7ebbe6303bef4a7ecfef832637491c9e1bbd265/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c6963656e73652f6869796f7567612f43686174474c4d2d456666696369656e742d54756e696e67" alt="GitHub 代码许可" data-canonical-src="https://img.shields.io/github/license/hiyouga/ChatGLM-Efficient-Tuning" style="max-width: 100%;"></a>
<a href="https://github.com/hiyouga/ChatGLM-Efficient-Tuning/commits/main"><img src="https://camo.githubusercontent.com/cb2aac33e41eb3aabe197414973dcf711f9316b8a037367d472e486cb38fa997/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c6173742d636f6d6d69742f6869796f7567612f43686174474c4d2d456666696369656e742d54756e696e67" alt="GitHub 最后一次提交" data-canonical-src="https://img.shields.io/github/last-commit/hiyouga/ChatGLM-Efficient-Tuning" style="max-width: 100%;"></a>
<a href="https://pypi.org/project/glmtuner/" rel="nofollow"><img src="https://camo.githubusercontent.com/0144b4436ef703d6a3124d6d17bc959aa4fc4f671ec272a3a94555c76960df0e/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f676c6d74756e6572" alt="皮伊" data-canonical-src="https://img.shields.io/pypi/v/glmtuner" style="max-width: 100%;"></a>
<a href="https://github.com/hiyouga/ChatGLM-Efficient-Tuning/pulls"><img src="https://camo.githubusercontent.com/05426382430092be65f7cb9c42eb64f05cdf054848d597274c0e2f1cf6214fe0/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5052732d77656c636f6d652d626c7565" alt="GitHub 拉取请求" data-canonical-src="https://img.shields.io/badge/PRs-welcome-blue" style="max-width: 100%;"></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><a href="https://github.com/huggingface/peft"><font style="vertical-align: inherit;">使用 🤗 PEFT</font></a><font style="vertical-align: inherit;">微调 &ZeroWidthSpace;&ZeroWidthSpace;🤖 </font></font><a href="https://github.com/THUDM/ChatGLM-6B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGLM-6B</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模型</font><font style="vertical-align: inherit;">。</font></font><a href="https://github.com/huggingface/peft"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">👋加入我们的</font></font><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/assets/wechat.jpg"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微信</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[ 英文 |</font></font><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/README_zh.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中文</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">]</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您有任何疑问，请参阅我们的</font></font><a href="https://github.com/hiyouga/ChatGLM-Efficient-Tuning/wiki"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Wiki📄</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意</font></font></h2><a id="user-content-notice" class="anchor" aria-label="永久链接：通知" href="#notice"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该回购协议</font><font style="vertical-align: inherit;">将来</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">不会被维护</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。请关注</font></font><strong><a href="https://github.com/hiyouga/LLaMA-Factory"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LLaMA-Factory</font></font></a></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对语言模型（包括ChatGLM2-6B）进行微调。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">变更日志</font></font></h2><a id="user-content-changelog" class="anchor" aria-label="永久链接：变更日志" href="#changelog"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/07/15] 现在我们开发了一个用于训练、评估和推理的一体化 Web UI。尝试</font></font><code>train_web.py</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 Web 浏览器中微调 ChatGLM-6B 模型。感谢</font></font><a href="https://github.com/KanadeSiina"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">@KanadeSiina</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://github.com/codemayq"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">@codemayq</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在开发中所做的努力。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/07/09] 现在我们发布了</font></font><a href="https://github.com/hiyouga/FastEdit"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FastEdit</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> ⚡🩹，一个易于使用的软件包，用于高效编辑大型语言模型的事实知识。</font><font style="vertical-align: inherit;">感兴趣的话</font><font style="vertical-align: inherit;">请关注</font></font><a href="https://github.com/hiyouga/FastEdit"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FastEdit 。</font></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/06/25] 现在，我们将</font></font><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/src/api_demo.py"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">演示 API</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">与</font></font><a href="https://platform.openai.com/docs/api-reference/chat" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI 的</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">格式保持一致，您可以在任意基于 ChatGPT 的应用程序中插入微调后的模型。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/THUDM/ChatGLM2-6B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/06/25] 现在我们支持使用我们的框架对ChatGLM2-6B</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模型进行微调</font><font style="vertical-align: inherit;">！</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/06/05] 现在我们支持 4 位 LoRA 训练（又名</font></font><a href="https://github.com/artidoro/qlora"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">QLoRA</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）。尝试</font></font><code>--quantization_bit 4</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 4 位量化模型进行论证。 （实验特征）</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/06/01] 我们实现了一个支持 LLaMA 和 BLOOM 模型高效调整的框架。</font><font style="vertical-align: inherit;">如果您有兴趣，</font><font style="vertical-align: inherit;">请关注</font></font><a href="https://github.com/hiyouga/LLaMA-Efficient-Tuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LLaMA-Efficient-Tuning 。</font></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/05/19] 现在我们支持在训练时使用开发集来评估模型。 Try</font></font><code>--dev_ratio</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数指定开发集的大小。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/04/29] 现在我们支持</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用人类反馈强化学习（RLHF）来</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">训练 ChatGLM ！我们提供了几个运行 RLHF 训练的示例，请参阅</font></font><code>examples</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件夹了解详细信息。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[2020年4月23日] 我们的仓库在12天内获得了100颗星！恭喜！</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/04/19] 现在我们支持合并</font><font style="vertical-align: inherit;">LoRA训练的微调模型的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">权重</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">！尝试</font></font><code>--checkpoint_dir checkpoint1,checkpoint2</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">论证不断微调模型。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/04/18] 现在我们支持</font><font style="vertical-align: inherit;">使用三种微调方法来训练</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化模型</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">！尝试</font></font><code>quantization_bit</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以 4/8 位训练模型。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/04/12] 现在我们支持</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">检查点训练</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">！使用</font></font><code>--checkpoint_dir</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数指定要从中进行微调的检查点模型。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[23/04/11] 现在我们支持使用</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">组合数据集</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">进行训练！尝试</font></font><code>--dataset dataset1,dataset2</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用多个数据集进行训练的论据。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据集</font></font></h2><a id="user-content-datasets" class="anchor" aria-label="永久链接：数据集" href="#datasets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于监督微调：
</font></font><ul dir="auto">
<li><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">斯坦福羊驼毛 (zh)</font></font></a></li>
<li><a href="https://github.com/ymcui/Chinese-LLaMA-Alpaca"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">斯坦福羊驼 (zh)</font></font></a></li>
<li><a href="https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPT-4 生成的数据（en&amp;zh）</font></font></a></li>
<li><a href="https://huggingface.co/datasets/OpenAssistant/oasst1" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">打开助手（多语言）</font></font></a></li>
<li><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/data/self_cognition.json"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自我认知 (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/QingyiSi/Alpaca-CoT/tree/main/Chinese-instruction-collection" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分享GPT (zh)</font></font></a></li>
<li><a href="https://github.com/sufengniu/RefGPT"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参考GPT (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/JosephusCheung/GuanacoDataset" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">原驼数据集（多语言）</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/train_2M_CN" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百丽 2M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/train_1M_CN" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百丽 1M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/train_0.5M_CN" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百丽 0.5M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/generated_chat_0.4M" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">美女对话0.4M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/school_math_0.25M" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百丽学校数学 0.25M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/BelleGroup/multiturn_chat_0.8M" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">BELLE 多轮聊天 0.8M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/YeungNLP/firefly-train-1.1M" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">萤火虫 1.1M (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/GAIR/lima" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">利马 (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/sahil2801/CodeAlpaca-20k" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CodeAlpaca 20k（en）</font></font></a></li>
<li><a href="https://huggingface.co/datasets/QingyiSi/Alpaca-CoT" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">羊驼 CoT（多语言）</font></font></a></li>
<li><a href="https://huggingface.co/datasets/suolyer/webqa" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">网络质量检查 (zh)</font></font></a></li>
<li><a href="https://github.com/thunlp/UltraChat"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">UltraChat（zh）</font></font></a></li>
<li><a href="https://huggingface.co/datasets/zxbsmk/webnovel_cn" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">网络小说 (zh)</font></font></a></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于奖励建模：
</font></font><ul dir="auto">
<li><a href="https://huggingface.co/datasets/Anthropic/hh-rlhf" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">HH-RLHF (zh)</font></font></a></li>
<li><a href="https://huggingface.co/datasets/OpenAssistant/oasst1" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">打开助手（多语言）</font></font></a></li>
<li><a href="https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPT-4 生成的数据（en&amp;zh）</font></font></a></li>
</ul>
</li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">详情</font><font style="vertical-align: inherit;">请参考</font></font><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/data/README.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">data/README.md 。</font></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">某些数据集在使用前需要确认，因此我们建议使用这些命令使用您的 Hugging Face 帐户登录。</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install --upgrade huggingface_hub
huggingface-cli login</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install --upgrade huggingface_hub
huggingface-cli login" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调方法</font></font></h2><a id="user-content-fine-tuning-methods" class="anchor" aria-label="永久链接：微调方法" href="#fine-tuning-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的脚本现在支持以下微调方法：</font></font></p>
<ul dir="auto">
<li><a href="https://arxiv.org/abs/2106.09685" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">洛拉</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调模型的低级适配器。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/THUDM/P-tuning-v2"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">P-调音V2</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调模型的前缀编码器。</font></font></li>
</ul>
</li>
<li><a href="https://arxiv.org/abs/2012.14913" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">冻结</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调模型最后 n 个块中的 MLP。</font></font></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">全面调整
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调模型的所有参数。</font></font></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要求</font></font></h2><a id="user-content-requirement" class="anchor" aria-label="永久链接： 要求" href="#requirement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python 3.8+ 和 PyTorch 1.13.1+</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🤗Transformers、数据集、Accelerate、PEFT 和 TRL</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">fire、protobuf、cpm 内核和句子</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">jieba、rouge-chinese 和 nltk（评估时使用）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">gradio 和 matplotlib（在 train_web.py 中使用）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">uvicorn、fastapi 和 sse-starlette（在 api_demo.py 中使用）</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">还有</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">强大的 GPU</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">！</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">入门</font></font></h2><a id="user-content-getting-started" class="anchor" aria-label="永久链接：开始使用" href="#getting-started"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据准备（可选）</font></font></h3><a id="user-content-data-preparation-optional" class="anchor" aria-label="永久链接：数据准备（可选）" href="#data-preparation-optional"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请参阅</font></font><code>data/example_dataset</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">查看有关数据集文件格式的详细信息。您可以使用单个</font></font><code>.json</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件或包含多个文件的</font></font><a href="https://huggingface.co/docs/datasets/dataset_script" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据集加载脚本</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来创建自定义数据集。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：请更新</font></font><code>data/dataset_info.json</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以使用您的自定义数据集。关于该文件的格式，请参考</font></font><code>data/README.md</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">依赖安装（可选）</font></font></h3><a id="user-content-dependence-installation-optional" class="anchor" aria-label="永久链接：依赖安装（可选）" href="#dependence-installation-optional"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>git lfs install
git clone https://github.com/hiyouga/ChatGLM-Efficient-Tuning.git
conda create -n chatglm_etuning python=3.10
conda activate chatglm_etuning
<span class="pl-c1">cd</span> ChatGLM-Efficient-Tuning
pip install -r requirements.txt</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git lfs install
git clone https://github.com/hiyouga/ChatGLM-Efficient-Tuning.git
conda create -n chatglm_etuning python=3.10
conda activate chatglm_etuning
cd ChatGLM-Efficient-Tuning
pip install -r requirements.txt" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果要在Windows平台上启用量化LoRA（QLoRA），则需要安装预构建版本的</font></font><code>bitsandbytes</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">库，该库支持CUDA 11.1至12.1。</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install https://github.com/jllllll/bitsandbytes-windows-webui/releases/download/wheels/bitsandbytes-0.39.1-py3-none-win_amd64.whl</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install https://github.com/jllllll/bitsandbytes-windows-webui/releases/download/wheels/bitsandbytes-0.39.1-py3-none-win_amd64.whl" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">一体化 Web 用户界面</font></font></h3><a id="user-content-all-in-one-web-ui" class="anchor" aria-label="永久链接：一体化 Web UI" href="#all-in-one-web-ui"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_web.py</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_web.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目前，Web UI 仅支持在</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">单个 GPU</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">上进行训练。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用单个 GPU 进行微调</font></font></h3><a id="user-content-fine-tuning-with-a-single-gpu" class="anchor" aria-label="永久链接：使用单个 GPU 进行微调" href="#fine-tuning-with-a-single-gpu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --output_dir path_to_sft_checkpoint \
    --per_device_train_batch_size 4 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 5e-5 \
    --num_train_epochs 3.0 \
    --plot_loss \
    --fp16</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --output_dir path_to_sft_checkpoint \
    --per_device_train_batch_size 4 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 5e-5 \
    --num_train_epochs 3.0 \
    --plot_loss \
    --fp16" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关参数的详细信息，</font><font style="vertical-align: inherit;">请参阅我们的</font></font><a href="https://github.com/hiyouga/ChatGLM-Efficient-Tuning/wiki"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Wiki 。</font></font></a><font style="vertical-align: inherit;"></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用多个 GPU 进行分布式微调</font></font></h3><a id="user-content-distributed-fine-tuning-with-multiple-gpus" class="anchor" aria-label="永久链接：使用多个 GPU 进行分布式微调" href="#distributed-fine-tuning-with-multiple-gpus"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>accelerate config <span class="pl-c"><span class="pl-c">#</span> configure the environment</span>
accelerate launch src/train_bash.py <span class="pl-c"><span class="pl-c">#</span> arguments (same as above)</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="accelerate config # configure the environment
accelerate launch src/train_bash.py # arguments (same as above)" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">培训奖励模型</font></font></h3><a id="user-content-training-reward-model" class="anchor" aria-label="永久链接：培训奖励模型" href="#training-reward-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage rm \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset comparison_gpt4_en \
    --finetuning_type lora \
    --resume_lora_training False \
    --checkpoint_dir path_to_sft_checkpoint \
    --output_dir path_to_rm_checkpoint \
    --per_device_train_batch_size 4 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 1e-5 \
    --num_train_epochs 1.0 \
    --plot_loss \
    --fp16</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage rm \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset comparison_gpt4_en \
    --finetuning_type lora \
    --resume_lora_training False \
    --checkpoint_dir path_to_sft_checkpoint \
    --output_dir path_to_rm_checkpoint \
    --per_device_train_batch_size 4 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 1e-5 \
    --num_train_epochs 1.0 \
    --plot_loss \
    --fp16" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RLHF 训练</font></font></h3><a id="user-content-training-with-rlhf" class="anchor" aria-label="永久链接：使用 RLHF 进行训练" href="#training-with-rlhf"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage ppo \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --resume_lora_training False \
    --checkpoint_dir path_to_sft_checkpoint \
    --reward_model path_to_rm_checkpoint \
    --output_dir path_to_ppo_checkpoint \
    --per_device_train_batch_size 2 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 1e-5 \
    --num_train_epochs 1.0 \
    --plot_loss</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage ppo \
    --model_name_or_path path_to_your_chatglm_model \
    --do_train \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --resume_lora_training False \
    --checkpoint_dir path_to_sft_checkpoint \
    --reward_model path_to_rm_checkpoint \
    --output_dir path_to_ppo_checkpoint \
    --per_device_train_batch_size 2 \
    --gradient_accumulation_steps 4 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --learning_rate 1e-5 \
    --num_train_epochs 1.0 \
    --plot_loss" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">评估（BLEU 和 ROUGE_CHINESE）</font></font></h3><a id="user-content-evaluation-bleu-and-rouge_chinese" class="anchor" aria-label="永久链接：评估（BLEU 和 ROUGE_CHINESE）" href="#evaluation-bleu-and-rouge_chinese"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_eval \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_eval_result \
    --per_device_eval_batch_size 8 \
    --max_samples 50 \
    --predict_with_generate</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_eval \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_eval_result \
    --per_device_eval_batch_size 8 \
    --max_samples 50 \
    --predict_with_generate" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">预测</font></font></h3><a id="user-content-predict" class="anchor" aria-label="永久链接：预测" href="#predict"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_predict \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_predict_result \
    --per_device_eval_batch_size 8 \
    --max_samples 100 \
    --predict_with_generate</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="CUDA_VISIBLE_DEVICES=0 python src/train_bash.py \
    --stage sft \
    --model_name_or_path path_to_your_chatglm_model \
    --do_predict \
    --dataset alpaca_gpt4_en \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_predict_result \
    --per_device_eval_batch_size 8 \
    --max_samples 100 \
    --predict_with_generate" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您想预测具有空响应的样本，请在该</font></font><code>response</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">列中填充</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">虚拟标记，</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以确保样本在整个预处理阶段不会被丢弃。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">API演示</font></font></h3><a id="user-content-api-demo" class="anchor" aria-label="永久链接：API 演示" href="#api-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python src/api_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python src/api_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">访问</font></font><code>http://localhost:8000/docs</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">API 文档。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CLI 演示</font></font></h3><a id="user-content-cli-demo" class="anchor" aria-label="永久链接：CLI 演示" href="#cli-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python src/cli_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python src/cli_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">网络演示</font></font></h3><a id="user-content-web-demo" class="anchor" aria-label="永久链接：网络演示" href="#web-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python src/web_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python src/web_demo.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">出口型号</font></font></h3><a id="user-content-export-model" class="anchor" aria-label="永久链接：出口模型" href="#export-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python src/export_model.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_export</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python src/export_model.py \
    --model_name_or_path path_to_your_chatglm_model \
    --finetuning_type lora \
    --checkpoint_dir path_to_checkpoint \
    --output_dir path_to_export" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">硬件要求</font></font></h3><a id="user-content-hardware-requirements" class="anchor" aria-label="永久链接：硬件要求" href="#hardware-requirements"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调方法</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量大小</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模式</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">公克</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">速度</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">28GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">24GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">20GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">10GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">P 调整 (p=16)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">20GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">P 调整 (p=16)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16 GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">P 调整 (p=16)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">12GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">冻结 (l=3)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">24GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8次/秒</font></font></td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RM法</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量大小</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模式</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">公克</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">速度</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8) + rm</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">22GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8) + rm</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">11GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-</font></font></td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RLHF法</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量大小</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模式</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">公克</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">速度</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8) + ppo</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FP16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">23GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8) + ppo</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">INT8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">12GB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">-</font></font></td>
</tr>
</tbody>
</table>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：</font></font><code>r</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是 lora 排名，</font></font><code>p</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是前缀标记的数量，</font></font><code>l</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是可训练层的数量，</font></font><code>ex/s</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是训练时每秒的示例数。设置</font></font><code>gradient_accumulation_steps</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为</font></font><code>1</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。所有这些都是在单个 Tesla V100 (32G) GPU 上进行评估的，它们是近似值，并且在不同的 GPU 中可能会有所不同。</font></font></p>
</blockquote>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调 ChatGLM：一个案例</font></font></h2><a id="user-content-fine-tuning-chatglm-a-case" class="anchor" aria-label="永久链接：微调 ChatGLM：一个案例" href="#fine-tuning-chatglm-a-case"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">培训结果</font></font></h3><a id="user-content-training-results" class="anchor" aria-label="永久链接：培训结果" href="#training-results"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们使用整个</font></font><code>alpaca_gpt4_zh</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据集，使用默认的超参数，通过 LoRA (r=8) 对 ChatGLM 模型进行一个 epoch 的微调。训练期间的损失曲线如下所示。</font></font></p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/assets/trainer_state.jpg"><img src="/hiyouga/ChatGLM-Efficient-Tuning/raw/main/assets/trainer_state.jpg" alt="训练损失" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">评估结果</font></font></h3><a id="user-content-evaluation-results" class="anchor" aria-label="永久链接：评估结果" href="#evaluation-results"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们在数据集中选择 100 个实例</font></font><code>alpaca_gpt4_zh</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来评估微调的 ChatGLM 模型并计算 BLEU 和 ROUGE 分数。结果如下。</font></font></p>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分数</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">原来的</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FZ (l=2)</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">PT (p=16)</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA (r=8)</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">BLEU-4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">15.75</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16.85</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16.06</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">17.01 ( </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">+1.26</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">胭脂-1</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">34.51</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">36.62</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">34.80</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">36.77 ( </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">+2.26</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">胭脂2号</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">15.11</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">17.04</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">15.32</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16.83 ( </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">+1.72</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">胭脂-l</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.18</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">28.17</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.35</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">28.86 ( </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">+2.68</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> )</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数 (%)</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">/</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4.35%</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">0.06%</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">0.06%</font></font></td>
</tr>
</tbody>
</table>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FZ：冻结调整，PT：P-Tuning V2（我们用于</font></font><code>pre_seq_len=16</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">与 LoRA 进行公平比较），Params：可训练参数的百分比。</font></font></p>
</blockquote>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">项目</font></font></h2><a id="user-content-projects" class="anchor" aria-label="永久链接：项目" href="#projects"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://github.com/SupritYoung/RLHF-Label-Tool/tree/master"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SupritYoung/RLHF-Label-Tool</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：一种对法学硕士的响应进行排名的工具，以生成用于 RLHF 培训的带注释样本。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">与现有实现相比</font></font></h2><a id="user-content-compared-with-existing-implementations" class="anchor" aria-label="永久链接：与现有实现相比" href="#compared-with-existing-implementations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://github.com/THUDM/ChatGLM-6B/tree/main/ptuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">THUDM/聊天GLM-6B</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在</font><a href="https://aclanthology.org/D19-1321.pdf" rel="nofollow"><font style="vertical-align: inherit;">ADGEN数据集上使用</font></a></font><a href="https://github.com/THUDM/P-tuning-v2"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">P-Tuning v2</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调 ChatGLM 的正式实施</font><font style="vertical-align: inherit;">。</font></font><a href="https://aclanthology.org/D19-1321.pdf" rel="nofollow"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的微调脚本很大程度上依赖于它。我们进一步实现了</font></font><a href="https://arxiv.org/abs/2106.09685" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调优方法。此外，我们</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动态地</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将输入填充到批次中的最长序列而不是最大长度，以加速微调。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/mymusise/ChatGLM-Tuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">mymusise/ChatGLM-调整</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在</font><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;">斯坦福羊驼数据集上使用</font></a></font><a href="https://arxiv.org/abs/2106.09685" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调 ChatGLM 的非官方实现</font><font style="vertical-align: inherit;">。</font></font><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们从中借鉴了一些想法。我们的微调脚本将数据预处理部分</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">集成</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">到训练过程中，因此我们不需要在训练前生成预处理数据集。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/ssbuild/chatglm_finetuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ssbuild/chatglm_finetuning</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"></font><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在斯坦福羊驼</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">数据集上使用多种 PEFT 方法微调 ChatGLM 的非官方实现</font><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的微调脚本</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">纯粹</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用</font></font><a href="https://github.com/huggingface/transformers"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hugging Face 转换器</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实现，并且独立于</font></font><a href="https://github.com/ssbuild/deep_training"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">deep_training</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">框架。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/lich99/ChatGLM-finetune-LoRA"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">lich99/ChatGLM-finetune-LoRA</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在</font><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;">斯坦福羊驼数据集上使用</font></a></font><a href="https://arxiv.org/abs/2106.09685" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LoRA</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调 ChatGLM 的非官方实现</font><font style="vertical-align: inherit;">。</font></font><a href="https://github.com/tatsu-lab/stanford_alpaca"><font style="vertical-align: inherit;"></font></a><font style="vertical-align: inherit;"></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们使用</font></font><a href="https://github.com/huggingface/peft"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hugging Face PEFT</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来提供最先进的 PEFT 方法。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/liucongg/ChatGLM-Finetuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">liucongg/ChatGLM-微调</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 Freeze、LoRA 和 P-Tuning 等多种方法对工业数据集进行微调 ChatGLM 的非官方实现。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的目标是纳入更多的指令跟踪数据集来微调 ChatGLM 模型。</font></font></li>
</ul>
</li>
<li><a href="https://github.com/yanqiangmiffy/InstructGLM"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">yanqiangmiffy/InstructGLM</font></font></a>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调 ChatGLM 的非官方实现，探索 ChatGLM 在指令跟踪数据集上的能力。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的微调脚本将数据预处理部分集成到训练过程中。</font></font></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">去做</font></font></h2><a id="user-content-todo" class="anchor" aria-label="永久链接：待办事项" href="#todo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用</font></font><a href="https://github.com/hwchase17/langchain"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LangChain</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">轻松构建能够在微调的 ChatGLM 模型上利用外部知识的应用程序。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实施对齐算法来对齐人类偏好。
</font></font><ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""> <a href="https://github.com/microsoft/DeepSpeed/tree/master/blogs/deepspeed-chat"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RLHF</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"> <a href="https://github.com/GanjinZero/RRHF"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">右心室颤动</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"> <a href="https://github.com/OptimalScale/LMFlow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">筏</font></font></a></li>
</ul>
</li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"></font><a href="https://github.com/brightmart/nlp_chinese_corpus"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将中文数据</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">集</font><font style="vertical-align: inherit;">纳入训练集中。
</font></font><ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""> <a href="https://github.com/LianjiaTech/BELLE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">美女</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"> <a href="https://github.com/CLUEbenchmark/pCLUE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CLUE</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"> <a href="https://github.com/CLUEbenchmark/CLUECorpus2020"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">线索语料库</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""> <a href="https://huggingface.co/datasets/JosephusCheung/GuanacoDataset" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">原驼数据集</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""> <a href="https://huggingface.co/datasets/YeungNLP/firefly-train-1.1M" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">萤火虫数据集</font></font></a></li>
</ul>
</li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将</font></font><a href="https://openai.com/blog/chatgpt" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGPT</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://openai.com/research/gpt-4" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPT-4</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自聊天数据纳入训练集中。
</font></font><ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"> <a href="https://github.com/project-baize/baize-chatbot"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">白泽</font></font></a></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""> <a href="https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPT-4-法学硕士</font></font></a></li>
</ul>
</li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实施 Freeze-Tuning 和 P-Tuning 方法。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持多GPU微调。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">添加评估脚本。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从检查点加载。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">微调量化模型。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">编写一本关于如何使用此框架微调 ChatGLM 的指南。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">结合最先进的模型编辑算法。 （</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">例如</font></font><a href="https://arxiv.org/abs/2110.11309" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">修复</font></font></a></em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">合并</font></font><a href="https://huggingface.co/datasets/OpenAssistant/oasst1" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAssistant 对话数据集</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以进行 SFT 和对齐。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">纳入高质量中文教学数据集</font></font><a href="https://huggingface.co/datasets/BAAI/COIG" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">COIG</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执照</font></font></h2><a id="user-content-license" class="anchor" aria-label="永久链接：许可证" href="#license"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="/hiyouga/ChatGLM-Efficient-Tuning/blob/main/LICENSE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该存储库根据Apache-2.0 License</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获得许可</font><font style="vertical-align: inherit;">。请遵循</font></font><a href="https://github.com/THUDM/ChatGLM-6B/blob/main/MODEL_LICENSE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">型号许可</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 ChatGLM-6B 型号。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引文</font></font></h2><a id="user-content-citation" class="anchor" aria-label="永久链接：引文" href="#citation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果这项工作有帮助，请引用为：</font></font></p>
<div class="highlight highlight-text-bibtex notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">@Misc</span>{<span class="pl-en">chatglm-efficient-tuning</span>,
  <span class="pl-s">title</span> = <span class="pl-s"><span class="pl-pds">{</span>ChatGLM Efficient Tuning<span class="pl-pds">}</span></span>,
  <span class="pl-s">author</span> = <span class="pl-s"><span class="pl-pds">{</span>hiyouga<span class="pl-pds">}</span></span>,
  <span class="pl-s">howpublished</span> = <span class="pl-s"><span class="pl-pds">{</span>\url{https://github.com/hiyouga/ChatGLM-Efficient-Tuning}<span class="pl-pds">}</span></span>,
  <span class="pl-s">year</span> = <span class="pl-s"><span class="pl-pds">{</span>2023<span class="pl-pds">}</span></span>
}</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="@Misc{chatglm-efficient-tuning,
  title = {ChatGLM Efficient Tuning},
  author = {hiyouga},
  howpublished = {\url{https://github.com/hiyouga/ChatGLM-Efficient-Tuning}},
  year = {2023}
}" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">致谢</font></font></h2><a id="user-content-acknowledgement" class="anchor" aria-label="永久链接：致谢" href="#acknowledgement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此存储库受益于</font></font><a href="https://github.com/THUDM/ChatGLM-6B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGLM-6B</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><a href="https://github.com/mymusise/ChatGLM-Tuning"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGLM-Tuning</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://github.com/yuanzhoulvpi2017/zero_nlp"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Yuanzhoulvpi2017/zero_nlp</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。感谢他们的精彩作品。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">明星历史</font></font></h2><a id="user-content-star-history" class="anchor" aria-label="永久链接：明星历史" href="#star-history"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://camo.githubusercontent.com/a22362f5bf84e415fe43db6925ccff2987be716250ad2a9a064676a89b3e58cd/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d6869796f7567612f43686174474c4d2d456666696369656e742d54756e696e6726747970653d44617465"><img src="https://camo.githubusercontent.com/a22362f5bf84e415fe43db6925ccff2987be716250ad2a9a064676a89b3e58cd/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d6869796f7567612f43686174474c4d2d456666696369656e742d54756e696e6726747970653d44617465" alt="明星历史图" data-canonical-src="https://api.star-history.com/svg?repos=hiyouga/ChatGLM-Efficient-Tuning&amp;type=Date" style="max-width: 100%;"></a></p>
</article></div>
