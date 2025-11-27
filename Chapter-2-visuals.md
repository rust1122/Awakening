# 🎨 Chapter 2 · Visuals

![Scope](https://img.shields.io/badge/Scope-Introduction_only-ff69b4?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-Visuals_%26_Workflows-8A2BE2?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-English-2ea44f?style=for-the-badge)
![Hardware](https://img.shields.io/badge/Hardware-GPU_recommended-FFA500?style=for-the-badge)
[![Text Chapter](https://img.shields.io/badge/Chapter%201-Text%20Creation-34D399?style=for-the-badge)](./Chapter-1-text.md)
[![Glossary](https://img.shields.io/badge/Glossary-Quick-FFB020?style=for-the-badge)](#glossary-quick)

This chapter focuses on AI-assisted visual creation: image generation, editing, control, restoration, and video assistance. Introduction-only — practical workflows and a curated project list, not a full tutorial.

---

## 💡 What AI Helps With
- Text-to-Image (T2I) and Image-to-Image (I2I) generation
- Editing: inpainting, outpainting, local refinements, style transfer
- Composition control: depth/edge/pose/layout conditioning (ControlNet, SAM)
- Reference guidance: image prompt adapters and style preservation (IP-Adapter, LoRA)
- Restoration and upscaling: face repair, denoise, super-resolution
- Video assistance: short clips, motion stylization, storyboard iterations

## ✅ Recommended Projects (by Use)

### 🖥️ Generation UIs (No/Low-Code)
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) — node/graph-based workflow UI; modular and reproducible
- [AUTOMATIC1111 Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) — popular SD UI with rich extensions
- [InvokeAI](https://github.com/invoke-ai/InvokeAI) — streamlined SD toolkit with robust inpainting
- [Fooocus](https://github.com/lllyasviel/Fooocus) — simplified UX for SD, strong defaults

### 📚 Models & Libraries
- [Stable Diffusion (CompVis)](https://github.com/CompVis/stable-diffusion) — core open-source diffusion model
- [Diffusers (HF)](https://huggingface.co/docs/diffusers) — Python library for diffusion models; SD, SVD, ControlNet
- [ControlNet](https://github.com/lllyasviel/ControlNet) — conditioning via edges/depth/pose/segmentation
- [IP-Adapter](https://github.com/TencentARC/IP-Adapter) — image prompt guidance; style/content reference
- [Segment Anything (SAM)](https://github.com/facebookresearch/segment-anything) — universal segmentation; masks for precise edits

### 🧩 Assets, Models, and Prompts
- [Civitai](https://civitai.com/) — community models, LoRA, embeddings, styles
- [Hugging Face Hub](https://huggingface.co/) — official model and dataset hosting
- [Lexica](https://lexica.art/) — prompt and image search
- [PromptHero](https://prompthero.com/) — prompt gallery and references

### 🧪 Editing, Restoration, and Upscaling
- [RemBG](https://github.com/danielgatis/rembg) — background removal
- [GFPGAN](https://github.com/TencentARC/GFPGAN) — face restoration
- [CodeFormer](https://github.com/sczhou/CodeFormer) — face repair with fidelity control
- [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) — super-resolution/upscaling
- [DeOldify](https://github.com/jantic/DeOldify) — colorization and restoration of old photos

### 🎬 Video Generation & Post
- [Stable Video Diffusion](https://github.com/Stability-AI/stable-video-diffusion) — image-to-video diffusion
- [Runway (Gen-3)](https://runwayml.com/) — commercial video generation and stylization
- [Pika](https://pika.art/) — text/image to video for short clips
- [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) — grading, editing, and finishing

### 🧠 LoRA Training & Fine-Tuning
- [kohya_ss](https://github.com/bmaltais/kohya_ss) — LoRA/DreamBooth training scripts and GUI
- [sd-scripts](https://github.com/kohya-ss/sd-scripts) — advanced training recipes for SD

---

## 🧰 Minimal Viable Stack (Low Barrier)
- ComfyUI or AUTOMATIC1111 for generation
- Civitai for model/styles discovery
- RemBG for fast cutouts
- Real-ESRGAN for upscaling

## 🚀 Advanced Stack (More Capabilities)
- Diffusers + ControlNet + IP-Adapter + SAM for programmable pipelines
- ComfyUI modular graphs for reproducible multi-step workflows
- InvokeAI for robust inpainting and batch variations
- LoRA fine-tuning with kohya_ss on curated references

## 🔧 Selection Tips
- Hardware matters: diffusion benefits from modern GPUs; for CPUs, keep batch/steps small
- Licensing: check model and asset licenses for commercial use; avoid unclear sources
- Reproducibility: prefer graph/pipeline tools (ComfyUI, Diffusers) to track params and nodes
- Style fidelity: use IP-Adapter/LoRA for consistent look; employ ControlNet for structure control

## 🗂️ Example Workflow (Adjust as Needed)
1. Define concept and collect references (style, palette, composition)
2. Generate base images (T2I) with stable defaults
3. Use ControlNet (edge/depth/pose) to refine composition and layouts
4. Inpaint/outpaint to fix local regions; face restoration with GFPGAN/CodeFormer
5. Upscale with Real-ESRGAN; apply light grading; export variations
6. Optional: animate with Stable Video Diffusion; finish in DaVinci Resolve

## 📗 Glossary (Quick)
- T2I / I2I — text-to-image / image-to-image
- Inpainting / Outpainting — content-aware local edits / canvas expansion
- ControlNet — conditioning via structural maps (edge/pose/depth/segmentation)
- IP-Adapter — image-guided generation preserving style/content
- LoRA — lightweight fine-tuning for custom styles/subjects
- SAM — segmentation producing masks for precise edits
- Upscaling — super-resolution to increase final asset quality

## ℹ️ Notes
- This chapter is introduction-only and will evolve with practical workflows.
- Most tools are cross-platform; for best performance, use a recent NVIDIA GPU.

## 🙌 Support
[![Support](https://img.shields.io/badge/Support-Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/A0A21P7W2J)