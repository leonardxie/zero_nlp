# 介绍
基于`llama`模型框架从零训练一个中文大模型

# 背景和想法
1. `llama`：`facebook`泄漏出来的`llama`模型，不能商用。而且也没中文token，虽然很多国内大牛已经对其进行扩充了。
2. `chatglm-6b`： `chatglm-6b`模型权重也不能商用，但是对中文的支持能力，太顶了！
3. `因此产生了想法`：
   - 能不能把`chatglm-6b`的`tokenizer`直接拿过来，嫁接到任意一个开源的大模型框架上
   - 并基于这个大模型框架，从零训练一个中文模型。
   - 毕竟，原始的模型权重不能商用，那我自己训练一个模型权重，肯定没啥问题。
4. `数据`：基于`belle`给到的数据，整理了一份`491万`条的数据文件，间接的提供了数据处理模版和基础的通用数据。
5. `大小`：应对不同的硬件资源，可以手动对模型的大小进行调整（从`1b`到`7b`再到`130b`都可以， 硬件资源越丰富，模型就可以设置的越大）
6. `训练`：为了让模型可以在多个消费级显卡上跑起来、推理起来，在训练的时候，支持`模型并行`方式。







