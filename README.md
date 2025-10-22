# 📊 Marp Demo (CODEVERSE Theme)

Презентація створена за допомогою [Marp](https://marp.app/) з кастомною темою **Codeverse**.

---

## 🚀 Встановлення

1. Встановіть **Node.js** (рекомендується LTS, наприклад v18):
   👉 [Завантажити Node.js](https://nodejs.org/)

2. Встановіть **Marp CLI** глобально:

   ```bash
   npm install -g @marp-team/marp-cli
   ```

3. Клонувати цей репозиторій:

   ```bash
   git clone https://github.com/<username>/<repo>.git
   cd <repo>
   ```

---

## 🛠 Використання

### 🔹 Збірка HTML з кастомною темою

```bash
marp slides.md --theme themes/codeverse.css -o index.html --allow-local-files
```

### 🔹 Збірка PDF з кастомною темою

```bash
marp slides.md --theme themes/codeverse.css -o slides.pdf --allow-local-files
```

### 🔹 Перегляд у браузері (live server)

```bash
marp -s --theme themes/codeverse.css
```

Після цього відкрийте у браузері:
👉 [http://localhost:8080/slides.md](http://localhost:8080/slides.md)

---

## 📂 Структура проекту

```
.
├── slides.md               # основний файл презентації
├── themes/
│   └── codeverse.css       # кастомна тема
├── img/                    # картинки та іконки
│   ├── logo.png
│   ├── team/
│   └── tech/
└── README.md
```

---

## 🔄 Автоматична збірка (GitHub Actions)

Файл workflow: `.github/workflows/marp.yml`

```yaml
name: Build and Deploy Marp presentation

on:
  push:
    branches: [ "main" ]

permissions:
  contents: write
  pages: write

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install Marp CLI
        run: npm install -g @marp-team/marp-cli

      - name: Build HTML with custom theme
        run: marp slides.md --theme themes/codeverse.css -o index.html --allow-local-files

      - name: Build PDF with custom theme
        run: marp slides.md --theme themes/codeverse.css -o slides.pdf --allow-local-files

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_branch: gh-pages
          publish_dir: ./
```

---

## 🌐 Доступ до результатів

Після пушу у `main` збираються та публікуються файли:

- [index.html](https://<username>.github.io/<repo>/index.html) — презентація у браузері
- [slides.pdf](https://<username>.github.io/<repo>/slides.pdf) — PDF-версія для завантаження

---

## 💡 Корисні посилання

- [Marp CLI Documentation](https://github.com/marp-team/marp-cli)
- [Marp Themes Guide](https://marpit.marp.app/theme-css)
- [Google Fonts: Orbitron](https://fonts.google.com/specimen/Orbitron)
