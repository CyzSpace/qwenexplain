#通义千问学习
#config
GenerationConfig {
  "chat_format": "chatml",
  "do_sample": true,
  "eos_token_id": 151643,
  "max_new_tokens": 512,
  "max_window_size": 6144,
  "pad_token_id": 151643,
  "repetition_penalty": 1.1,
  "top_k": 0,
  "top_p": 0.8,
  "trust_remote_code": true
}
这是一个用于生成语言模型文本输出的配置，具体参数的含义如下：
1. chat_format:
指定聊天格式为 chatml。
chatml 是一种专用的格式，通常用于聊天或对话系统，可能与上下文格式和处理有关。
2. do_sample:
值为 true，表示生成时采用采样方式，而不是选择概率最高的结果（即不是完全贪心解码）。
这通常用于生成更丰富和多样化的文本。
3. eos_token_id:
表示生成结束的标志（End of Sequence, EOS）的标识符，这里设置为 151643。
当模型生成此标志符时，会停止生成。
4. max_new_tokens:
表示生成的最大新标记数，设置为 512。
限制模型在一次生成中最多生成 512 个新 token。
5. max_window_size:
指定上下文窗口的最大大小，设置为 6144。
这是模型在处理输入和生成时可以参考的最大 token 数。
6. pad_token_id:
表示填充标记（Padding）的标识符，设置为 151643。
通常用于对输入或生成的 token 序列进行对齐。
7. repetition_penalty:
设置为 1.1，用于减少重复内容的生成。
如果生成的 token 在上下文中已经出现，模型会根据惩罚系数调整其概率，从而减少重复。
8. top_k:
值为 0，表示禁用 Top-K 采样。
如果启用，模型会只从概率最高的 K 个候选 token 中采样。
9. top_p:
值为 0.8，表示启用核采样（nucleus sampling）。
模型会从累积概率不超过 0.8 的候选 token 中采样，进一步控制生成的多样性。
10. trust_remote_code:
值为 true，表示允许运行远程代码。
这可能是为了支持某些依赖远程实现的模型组件。
