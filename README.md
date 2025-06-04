### 🛠️ Modified `transformers/` Library

In local inference mode, we extend the internal decoding loop of the HuggingFace `transformers` library to support execution-aware generation.  
Specifically, our modifications in `transformers/generation/utils.py` enable token-level integration of runtime feedback, allowing the model to dynamically condition on execution traces — as described in [Section 3 of the paper](https://github.com/boazlavon/eg_cfg/tree/master).

> ✅ This work builds on the original [Hugging Face Transformers repository](https://github.com/huggingface/transformers), which is licensed under the Apache License 2.0.  
> The original code remains under Apache 2.0.  
>
> 🔒 **Only the modifications introduced by the EG-CFG Research Team are licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)**.  
> These changes are clearly marked in the source code using `# --- EG-CFG Modification START ---` and `# --- EG-CFG Modification END ---` comment blocks.  
> For commercial use of these modifications, please contact [yair.eran@ramot.org](mailto:yair.eran@ramot.org).  
>
> Full source: [github.com/boazlavon/eg_cfg](https://github.com/boazlavon/eg_cfg/tree/master)
