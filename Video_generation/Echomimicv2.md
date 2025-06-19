# 🗣️ EchoMimic v2 – Audio-Driven Semi-Body Animation (Ant Group)

**EchoMimic v2** is an advanced **audio-driven half-body animation model** developed by Ant Group’s Terminal Technology Department. It offers a significant upgrade over the earlier version with greater **expressiveness**, **simplicity**, and **efficiency**.

---

## 🔑 What Makes EchoMimic v2 Stand Out

### 1. 🧠 Audio–Pose Dynamic Harmonization (APDH)

- **Pose Sampling**: Dynamically reduces dependency from full-body to mouth- or hand-specific poses, ensuring natural movement with fewer inputs.
- **Audio Diffusion**: Audio influences not only lips but also gestures and posture, thanks to dynamic motion conditioning.

---

### 2. 🧍 Semi-Body Animation

- EchoMimic v2 goes beyond head-only avatars.
- Outputs synchronized **upper-body** motion including **facial expressions** and **arm/gesture movement**.

---

### 3. 🎯 Head Partial Attention & Data Augmentation

- Trained using only **headshot images**.
- Can generate full half-body motion during inference using only a **reference image + audio**.

---

### 4. 🔄 Phase‑Specific Denoising Loss (PhD Loss)

Training is divided into **phases** for enhanced output:

- ✨ Pose clarity
- 🧽 Fine-grained detail refinement
- 💅 Low-level visual polish

> Results in smoother, expressive, and visually rich animations.

---

## 🛠️ Strengths & Limitations

### ✅ Strengths

- Realistic lip sync + upper-body gestures
- Requires **minimal input** (reference image + audio)
- No need for external pose maps
- Works well with **portrait images**
- Efficient pipeline with expressive results

---

### ⚠️ Limitations

- Requires **strong GPU** (≥24 GB VRAM recommended)
- Pose sync not end-to-end; uses default poses if none provided
- Best performance with **cropped face/upper-body images**, not full-body

---

## 🚀 How to Use EchoMimic v2

### 📦 Access

- **Open-source** on:
  - [GitHub](https://github.com/antgroup/echomimic_v2)
  - [Hugging Face](https://huggingface.co)

- Supported in:
  - 🧩 **ComfyUI**
  - 🌐 **Gradio workflows**

---

### 🖥️ Local Installation

```bash
git clone https://github.com/antgroup/echomimic_v2
cd echomimic_v2
# Follow the GPU setup instructions
# Run inference using your reference image, audio, and optional pose
