# 📊 Marp Demo (CODEVERSE Theme)

Presentation created with [Marp](https://marp.app/) using a custom **Codeverse** theme.

---

## 🚀 Installation

1. Install **Node.js** (LTS recommended, e.g. v18):
   👉 [Download Node.js](https://nodejs.org/)

2. Install **Marp CLI** globally:

   ```bash
   npm install -g @marp-team/marp-cli
   ```

3. Clone this repository:

   ```bash
   git clone https://github.com/<username>/<repo>.git
   cd <repo>
   ```

---

## 🛠 Usage

### 🔹 Build HTML with custom theme

```bash
marp slides.md --theme themes/codeverse.css -o index.html
```

### 🔹 Build PDF with custom theme

```bash
marp slides.md --theme themes/codeverse.css -o slides.pdf --allow-local-files
```

### 🔹 Live preview in browser

```bash
marp -s --theme themes/codeverse.css
```

Then open in your browser:
👉 [http://localhost:8080/index.html](http://localhost:8080/index.html)

---

## 📂 Project Structure

```
.
├── slides.md               # main presentation file
├── themes/
│   └── codeverse.css       # custom theme
├── img/                    # images and icons
│   ├── logo.png
│   ├── team/
│   └── tech/
└── README.md
```

---

## 🔄 Automatic Build (GitHub Actions)

Workflow file: `.github/workflows/marp.yml`

---

## 🌐 Access the Results

After pushing to `main`, files are built and published automatically:

- [index.html](https://<username>.github.io/<repo>/index.html) — presentation in browser
- [slides.pdf](https://<username>.github.io/<repo>/slides.pdf) — downloadable PDF version

---

## 💡 Useful Links

- [Marp CLI Documentation](https://github.com/marp-team/marp-cli)
- [Marp Themes Guide](https://marpit.marp.app/theme-css)
- [Google Fonts: Orbitron](https://fonts.google.com/specimen/Orbitron)
