# Technical Artist — Tech Test
**Luis Hostos**

---

## 🔗 Links

| | |
|---|---|
| **Repository** | https://github.com/BuhoNero/ta-tech-test |
| **Branch** | `polish/play-button` |
| **Pull Request** | https://github.com/BuhoNero/ta-tech-test/pull/1 |

---

## 📁 Project Structure

The original project folder structure corresponds to a Unity package downloaded from the Asset Store. While the structure is well-defined, working directly in it presents a risk — assets could be accidentally overwritten when reimporting or updating the package.

Following best practices, I created a clean, separate folder structure:
```
Project/
├── Animations/
├── Audio/
│   └── SFX/
├── Materials/
├── Prefabs/
├── Scenes/
└── Textures/
```

I also created a Unity scene called **Main** for the test itself.

---

## ✨ Game Juice

Animations were added to several UI elements, as shown in the demo scene.

A third-party extension was imported to support Particle Systems on UI canvases:
👉 [ParticleEffectForUGUI](https://github.com/mob-sakai/ParticleEffectForUGUI)

---

## 🖼️ UI

- Removed buttons that weren't visible
- Created new prefabs and reorganized the hierarchy slightly to accommodate the required animations and SFX

---

## ⚡ Performance Optimization

The scene is very light at this stage — approximately **29 draw calls** and high FPS in the PC editor. No significant optimization is needed yet.

**Potential improvement:** Sprite Atlases could be used if individual sprites multiply — packing them into a single power-of-two texture enables better compression.

---

## 🔧 Pipeline Optimization

Artists should have basic training on exporting assets for Unity. Key recommendations:

- **Target resolution** — Work at the exact resolution needed for the target device (e.g. mobile)
- **Slicing** — Prepare buttons, panels, and backgrounds for 9-slice or other common slice configurations
- **Dynamic coloring** — Export assets that need runtime tinting in grayscale
- **Compression-friendly textures** — Use power-of-two sizes where possible
- **Aspect ratio support** — Design UI assets to adapt across multiple screen ratios

**Workflow tip:** For a 2D sprite-based project, I would create a **Texture Import Settings preset** and set it as the project default — this ensures every imported texture is automatically configured as a 2D Sprite, saving time and reducing inconsistencies.
