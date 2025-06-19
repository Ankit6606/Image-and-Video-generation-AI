# 🎬 Runway Gen-2: Reference-Based Video Generation

**Runway Gen-2** supports reference-based video generation, enabling users to guide video creation using **images, videos, and text** — similar to **Midjourney’s Omni-Reference**, but for **motion content**.

---

## 🧠 What Is Reference-Based Generation in Runway?

In **Runway Gen-2**, you can:

- 🖼️ Provide an **image** or 🎞️ **video** as reference
- 💬 Add a **text prompt** to describe transformations
- ✅ Generate a new video blending both inputs

### ✨ Example Prompt:
> “Use this image of a forest, and make it a magical night scene with glowing plants.”

---

## 🧠 Types of Reference Inputs in Runway

| Input Type     | Purpose                        | Example Use                        |
|----------------|--------------------------------|-------------------------------------|
| 🖼️ **Image**      | Style, composition, character | Turn a concept art into video       |
| 🎞️ **Video**      | Motion, scene pacing          | Stylize or extend an existing clip  |
| 💬 **Text Prompt** | Semantic guidance             | Add effects or change visual themes |

> ✅ Combine all three for full creative control

---

## 🛠️ How to Use It (GUI)

1. Visit: [https://runwayml.com/](https://runwayml.com/)
2. Choose **Gen-2**
3. Select:
   - **Image + Text to Video**, or
   - **Video to Video**
4. Upload your reference image or video
5. Enter your descriptive **text prompt**
6. Click **Generate**

> Output: Short video (~3–4 seconds)

---

## 📌 Example Use Cases

| Reference Type | Prompt                            | Output                                 |
|----------------|-----------------------------------|----------------------------------------|
| 🖼️ **Image**      | “Turn this sketch into 3D render” | Photorealistic animated version        |
| 🎞️ **Video**      | “Same scene but at night”        | Day-to-night stylized animation        |
| 💬 **Text**       | “Add snowfall and glowing lights”| Effects layered on top of reference    |

---

## ⚙️ Advanced Options

- 🌀 **Interpolation** between frames
- 🎨 **Style transfer** from reference video
- 🎞️ **Frame-by-frame control** (experimental via API)

---

## 🔓 Access Notes

- ❌ **Not open-source**
- ✅ **Free tier** available (limited exports)
- 🚀 **Pro/API tiers** support:
  - Higher resolution
  - Longer clips
