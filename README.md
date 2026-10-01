# ✨ Holographic Card

A shiny holographic card effect built with **HTML, CSS, and a little JavaScript**. Move your mouse over the card and a rainbow sheen follows your cursor.

No libraries, no frameworks. Just a few lines of clean code.


## 🎨 How It Works

The effect comes from three simple tricks:

- **`radial-gradient` that follows the mouse:** a small JavaScript listener updates two CSS variables, `--mx` and `--my`, with the cursor position. The gradient's center uses them, so the shine moves with your mouse.
- **`mix-blend-mode`:** blends the colorful gradient with the card underneath to create the holographic look.
- **CSS transitions:** the shine fades in smoothly on hover, using `--duration` and `--ease` variables.

```css
.card-shine {
  position: absolute;
  inset: 0;
  background: radial-gradient(
    circle 90px at var(--mx) var(--my),
    var(--holo-2),
    var(--holo-4) 30%,
    var(--holo-1) 55%,
    var(--holo-3) 75%,
    transparent 100%
  );
  mix-blend-mode: multiply;
  opacity: 0;
  transition: opacity var(--duration) var(--ease);
  pointer-events: none;
}
```

## 📁 Project Structure

```
holographic-card/
├── index.html   # the card markup
├── style.css    # styles and the holographic effect
└── script.js    # updates the mouse position variables
```

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/holographic-card.git
   ```
2. Open `index.html` in your browser.

That's it. No installation or build step needed.

## 🛠️ Customize It

All the main settings are CSS variables at the top of `style.css`. Change them to make the card your own:

| Variable | What it controls |
|---|---|
| `--holo-1` to `--holo-4` | The holographic colors |
| `--duration` | How fast the shine fades in |
| `--ease` | The animation easing |

Try swapping the colors for a gold, neon, or pastel version ✨

## 📄 License

Free to use in personal and commercial projects. A mention or a tag is always appreciated 🙌

---

Made with 💜 by [Your Name](https://your-profile-link). Follow for more CSS effects!
