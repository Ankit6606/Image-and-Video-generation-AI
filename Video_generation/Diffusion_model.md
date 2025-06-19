# 🎬 How Video Generators Using Diffusion Models Work

A **video diffusion model** generates a **video** (sequence of frames) by learning to reverse noise in both **space** (images) and **time** (motion).

> In simple terms: it starts with **random noise across frames**, and gradually turns it into a smooth, realistic video based on a prompt.

---

## 🧠 Core Process

### ✅ Step 1: Forward Process (Training Time)
- Start with real video clips (e.g., 16 frames of 512×512).
- Add **Gaussian noise** to every frame over time steps.
- Video becomes complete noise.
- This noise addition is *known and fixed*, not learned.

---

### ✅ Step 2: Reverse Process (Generation Time)
- Model learns to **denoise** the video step-by-step:
  - From random noise → realistic, coherent video.
- Uses a neural network (often a **3D U-Net**) that processes:
  - **Spatial features** (inside each frame),
  - **Temporal dynamics** (motion across frames),
  - **Prompt conditioning** (text guidance, if any).

---

## 🎥 Text-to-Video Example

### Prompt:
> “A panda surfing on a big ocean wave at sunset”

### Steps:
1. **Text Embedding**: Prompt is encoded via CLIP/T5.
2. **Noise Tensor**: A 4D tensor is generated: `[Frames, Height, Width, Channels]`, e.g. `[16, 512, 512, 3]`.
3. **Denoising**: Iteratively denoised over ~50–100 steps.
4. **Result**: 2–4 sec video (e.g., 16 frames at 8 fps).

---

## 🏗️ Key Components

| Component           | Role                                             |
| ------------------- | ------------------------------------------------ |
| **3D U-Net**        | Denoises both space and time                     |
| **Text Encoder**    | Encodes the input prompt                         |
| **Noise Scheduler** | Manages noise addition/removal steps             |
| **Cross Attention** | Injects prompt understanding into the video      |
| **Temporal Layers** | Ensure smooth motion across frames               |

---

## 🧰 Common Models & Tools

| Model              | Description                                      |
| ------------------ | ------------------------------------------------ |
| `ModelScope`       | Open-source, simple text-to-video model          |
| `Pika Labs`        | No-code web-based video generator                |
| `Sora` (OpenAI)    | Cutting-edge video diffusion with realism        |
| `Gen-2` (RunwayML) | Accepts text, images, or video input             |

---

## 🧪 Python Example (Hugging Face)

```python
from diffusers import DiffusionPipeline

pipe = DiffusionPipeline.from_pretrained("damo-vilab/text-to-video-ms-1.7b")
pipe.to("cuda")

video_frames = pipe("A panda surfing at sunset", num_inference_steps=30).frames
```
## 📦 Output

- Returns a list of frames (`PIL.Image` or `numpy.ndarray`).
- Frames can be saved or exported as:
  - `.gif`
  - `.mp4`
  - `.webm`, etc.

Example using `moviepy`:

```python
from moviepy.editor import ImageSequenceClip

clip = ImageSequenceClip(video_frames, fps=8)
clip.write_videofile("output_video.mp4")
```

## 📌 Summary

| Step             | Description                                     |
| ---------------- | ----------------------------------------------- |
| 1. Add noise     | Gaussian noise applied to each frame (training) |
| 2. Learn reverse | Model learns to denoise it (training)           |
| 3. Generate      | Start from noise, guide using prompt            |
| 4. Output        | Get a smooth, coherent short video              |

