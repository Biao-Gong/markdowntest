<h1 align="center">Ming-unify: Advancements in Unified Architecture for Natural Multimodal Interaction</h1>

<p align="center">
          🤗 <a href="https://github.com/inclusionAI/Ming/Ming-unify">Hugging Face</a>&nbsp&nbsp | &nbsp&nbsp🤖 <a href="https://github.com/inclusionAI/Ming/Ming-unify">ModelScope</a>&nbsp&nbsp | &nbsp&nbsp 📑 <a href="https://github.com/inclusionAI/Ming/Ming-unify">Paper</a>&nbsp&nbsp 
</p>

Core technical breakthroughs of this open-source project:

- **Unified Visual Understanding & Generation Architecture.** We introduce a shared representation space for vision-language tasks, replacing traditional CLIP+Diffusion pipelines. The architecture leverages **learnable multiscale-queries** that dynamically integrate multimodal signals, enabling seamless end-to-end sequence prediction for text→image→editing workflows. This approach effectively addresses the quality limitations of discrete token-based methods. Our Ming-unify achieves the unification of generation and understanding, with an average understanding score of 69.7 on the OpenCompass leaderboard, surpassing DeepSeek-VL2 (66.4). At the same time, it maintains strong generation capabilities, achieving a generation score of 61.9 on the GenEval benchmark, outperforming SDXL (0.55).
- **Multi-Scale Learnable Query Token.** 	We employs a novel mechanism to establish feature correlations across resolutions of 4×/8×/16×. By introducing **hierarchical tokens**, the model resolves cross-scale inconsistencies in super-resolution and editing tasks. 
- **Cross-Scale Consistency Loss.** A **cross-scale consistency loss** is applied, leveraging explicit gradient constraints to enhance high-resolution reconstruction quality by more than 2dB PSNR (validated at native resolution).
- **Connector Module.** We facilitates dynamic alignment of features between frozen MLLM and trainable Diffusion models, achieves semantic alignment for text-to-pixel generation while also ensuring local-global coherence in edits.
- **AGI-Capable System.** Our model supports complex chained operations, such as "generate castle → add sunset → adjust perspective," with a swift response time of under 1 second (benchmarked with RTX 4090). The system is designed to handle instruction-driven generation-editing and is synchronized with ChatGPT-4o(aligned with the industry milestone of March 2025).



## Why It Matters

Ming-unify's unified architecture overcomes fundamental limitations of conventional approaches:

| Conventional Methods | Ming-unify's Advantages |
|----------------------|------------------|
| **Modular Pipelines**<br>(CLIP/SigLIP + Diffusion Models) | **End-to-End Unified Model**<br>Seamless understanding-generation integration |
| **Discrete Token AR**<br>(Limited visual grounding) | **Continuous Token Space**<br>Native support for fine-grained visual concepts |
| **Fixed-Resolution Processing**<br>(Artifacts in upscaling) | **Multi-Scale Adaptation**<br>Consistent quality across resolutions |
| **Separate Editing Workflows**<br>(Manual alignment required) | **Dialog-Driven Control**<br>Natural language guided pixel-level editing |
| **Understanding Bottlenecks**<br>(Visual-semantic mismatch) | **Joint Representation Learning**<br>Mutually enhanced comprehension and generation |

## Open Collaboration
We're open-sourcing Ming-unify to accelerate progress toward AGI, featuring:
- 📂 Full model weights & test code  
- 🧩 Modular architecture for easy extension  
- 📊 Comprehensive benchmarks (vs GPT-4V, SDXL, etc.)

*"The simultaneous release of ChatGPT-4's image generation in March 2025 confirms our vision of unified multimodal AI as the next paradigm."*  

## Empowering Multimodal Interaction with Ming-unify
**Ming-unify** acts as a unified model for multimodal understanding, extending beyond traditional NLP tasks and multimodal comprehension to enable interactive multimodal generation. This includes capabilities such as image generation, image editing, and style transfer.

![Ming_unify_usecases](https://github.com/user-attachments/assets/125767e8-05b9-4f74-85fa-9fd682520ef1)


## Model Structure
**Ming-unify** is a unified multimodal model designed for both image understanding and high-fidelity image generation. It achieves this by compressing image representations into continuous visual tokens, which are processed alongside discrete text tokens using a scaled auto-regressive Transformer. The generation capability is powered by an externally trained diffusion model (SANA), conditioned on tokens produced by the Transformer.

<img width="1034" alt="B106FE9E-5839-48c3-A175-AE8A4D2D8BB8" src="https://github.com/user-attachments/assets/927e090e-7cda-4f32-81de-774466973077" />


## Example Usage
#### System Requirements
- **Python:** >= 3.8
- **PyTorch:** >= 2.4.1+cu12.2 (CUDA 12.2 compatible)

#### Installation

To set up the environment, use pip to install the following dependencies:

```bash
pip install torch==2.4.1
torchvision==0.16.2
torchaudio==2.4.0
tensorflow==2.13.1
numpy==1.24.4
pandas==2.0.1
scipy==1.10.1
scikit-learn==1.3.2
h5py==3.10.0
transformers==4.46.3
diffusers==0.33.0
datasets==2.15.0
sentence-transformers==3.2.1
tokenizers==0.20.3
safetensors==0.4.1
accelerate==0.33.0
deepspeed==0.16.0
bitsandbytes==0.39.0
flash-attn==2.6.3
peft==0.12.0
```

- ### Usage Guided
Below is an example of how to load and use the model:
```python
from transformers import AutoModel, AutoTokenizer

Load the model and tokenizer
model_name = "your-username/your-model-name"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModel.from_pretrained(model_name)

Example input
image_file = None
prompt = "Produce image: a smiling man with dark hair sits on a wooden bench wearing a black shirt, khaki pants, and a black belt he accessorizes with a silver and white watch"
generate_prefix = "Production done: <image>" 

Process outputs
print(outputs)
```
For more advanced usage, such as fine-tuning or generating images, refer to the documentation.




## Acknowledgments

The project is currently in its early stages. While some preliminary results have been promising, substantial progress is needed to achieve seamless integration of understanding and generation. Both the code and models require further refinement and optimization, which is why we have chosen to open-source the project. We invite contributions from the community to help enhance and develop it collaboratively. If you have any suggestions or identify issues within the code, please contribute via Pull Requests. Thank you for your support and interest!

## Contact Information

Please submit a GitHub issue if you want help or have issues using Ming.

## License

Ming is licensed under [the MIT License](https://github.com/inclusionAI/Ming/blob/master/LICENCE).

## Citation

If you find our work helpful, feel free to give us a cite.

```bibtex
@article{Mingunify2025,
    title   = {Ming-unify: Advancements in Unified Architecture for Natural Multimodal Interaction}, 
    author  = {Inclusion AI, Ant Group},
    journal = {arXiv preprint arXiv:},
    year    = {2025}
}
```
