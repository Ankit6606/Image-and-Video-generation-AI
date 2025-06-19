# 🎨 Midjourney Omni-Reference (v6.0+)

**Omni-Reference** is a powerful new feature in **Midjourney v6.0+** that lets you generate AI images by combining multiple references — including **images, styles, poses, and text** — into a single coherent output.

---

## 🧠 What Is “Omni-Reference”?

> Omni-reference = **Multi-modal input → Coherent image output**

You can input:
- Multiple image URLs (e.g., for style, pose, composition)
- A descriptive text prompt

### 🧩 It's like saying:
> “Use the **style of image A**, the **composition of image B**, and generate a **scene described by text C**.”

---

## 🔧 How It Works

### 🛠️ Prompt Format:

```arduino
/imagine image::style_image_url image::pose_image_url prompt text --v 6.0
```

Each `image::` tag acts like a **reference input**:

- `style_image_url` → Controls **style** (color, brushwork, tone)
- `pose_image_url` → Controls **character pose** or **layout**
- `scene_image_url` → Controls **lighting** or **mood**
- `prompt` → Adds **description** / **semantic intent**


## ✨ Example Prompt (Omni-Reference)

```arduino
/imagine image::https://i.imgur.com/style1.jpg image::https://i.imgur.com/pose1.jpg A samurai warrior walking through a neon-lit street at night --v 6.0 --ar 16:9
```

## 🧠 How Midjourney Combines References

Midjourney combines:

- 🎨 **Style** from the first image
- 🕴️ **Pose or layout** from the second image
- 📝 **Scene/subject** from your text prompt

---

## 📌 Key Features

| Feature             | Description                                             |
|---------------------|---------------------------------------------------------|
| 🔗 **Multi-Image Input** | Supports multiple image URLs                         |
| 🎨 **Style Control**     | Use an image to guide color, brush, or tone          |
| 🕴️ **Pose/Body Ref**     | Use a photo to guide body language or structure      |
| 📜 **Prompt-Image Blend**| Text + image cues fused into one coherent output     |
| 🧠 **Smart Weighting**   | Automatically balances reference strength (no `--iw`) |

---

## ✅ Benefits

- Greater control over image output
- Easier to replicate a specific look or feel
- Ideal for:
  - 🎭 Character design
  - 👗 Fashion mockups
  - 📦 Product visualizations
  - 🎬 Cinematic frames

---

## ⚠️ Limitations

- Only available in **Midjourney v6.0+** (via Discord)
- Requires **URL-accessible images** (e.g., Imgur or CDN links)
- Does **not** support real-time pose detection (but gets close)
- Cannot upload **PSD files** or **layer maps** (yet)
