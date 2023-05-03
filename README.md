<p align="center" width="100%">
<img src="./image.png" alt="OpenAlpaca" style="width: 50%; min-width: 300px; display: block; margin: auto;">
</p>

# OpenAlpaca: An Open-source Instruction-following OpenLLaMA Model That Can Be Commercially Used

![Data License](https://img.shields.io/badge/Data-CC%20BY--SA%203.0-red.svg)
![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)
![Model Weight License](https://img.shields.io/badge/Model_Weights%20License-Apache_2.0-green.svg)

**Team:** [Yixuan Su](https://yxuansu.github.io/)<sup>\*</sup>, [Tian Lan](https://github.com/gmftbyGMFTBY)<sup>\*</sup>, and [Deng Cai](https://jcyk.github.io/)<sup>\*</sup> (all members contributed equally)

This is the repo for the OpenAlpaca project, which aims to build and share an instruction-following model based on [OpenLLaMA](https://github.com/openlm-research/open_llama). We note that, following OpenLLaMA, OpenAlpaca is permissively licensed under [the Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0). This repo contains

- The <a href='#data'>data</a> used for fine-tuning the model.
- The <a href='#code'>code</a> for fine-tuning the model.
- The <a href='#weights'>weights</a> for the fine-tuned model.
- The <a href='#example_usage'>example usage</a> of OpenAlpaca.

**Usage and License Notices:** OpenAlpaca follows the distribution permission of [OpenLLaMA](https://github.com/openlm-research/open_llama), i.e. the Apache 2.0 license, which means OpenAlpaca can be used in any academic or commercial purposes for free.


****

<span id='data'/>

# Data:

The data, i.e. [openalpaca.json](https://github.com/yxuansu/OpenAlpaca/blob/main/openalpaca.json), we use to fine-tune the model contains ~15k instances and is constructed from the [databricks-dolly-15k dataset](https://huggingface.co/datasets/databricks/databricks-dolly-15k) by removing samples that are too long. Following the original databricks-dolly-15k dataset, our data is also licensed under [the CC BY-SA 3.0 license](https://repositories.lib.utexas.edu/bitstream/handle/2152/11616/license_text?sequence=2&isAllowed=y) which allows it to be used in any academic and commerical purposes. 

**Format:** Following [Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca), our json file is a list of dictionaries, each one contains the following fields.
- `instruction`: it describes the task the model should perform.
- `input`: optional context or input for the task (e.g. the document for summarization task). 
- `output`: the answer to the instruction (and the optional input) which is written by human.

**Reproduce the data:** To reproduce the data, simply run `python3 process_dataset.py`.


<span id='code'/>

# Fine-tuning the Model:

<span id='weights'/>

# Model Weights:


<span id='example_usage'/>

# Example Usage:

<span id='future_plans'/>

# Future Plans:

1. The current OpenAlpaca_V1 (7B) model is fine-tuned on the previewed version of [OpenLLaMA](https://github.com/openlm-research/open_llama) (7B). The previewed version of OpenLLaMA (7B) is only trained with **200** billion tokens and we expect the performance of the base OpenLLaMA (7B) model to improve as the training continues. We will update the version of OpenAlpaca so long as newer checkpoint is released by the authors of OpenLLaMA.

2. We also plan to do a rigorous evaluation of OpenAlpaca and compare it with other publicly accessible models.
