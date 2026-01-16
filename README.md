---

# 🌐 i18n-Ready Next.js App

A starter template for building **multilingual (i18n) Next.js applications**. This template provides a clean structure, language-based routing, and ready-to-use translations.

---

## 🚀 Features

* Fully compatible with **Next.js 16+**
* Built-in **internationalization (i18n) support**
* **Language-based routing** for SEO-friendly URLs
* Pre-configured translation files for **Azerbaijani (AZ)** and **English (EN)**
* Easy to extend with new languages

---

## ⚡ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/faridmsta/i18n-ready-nextjs-app.git
cd i18n-ready-nextjs-app
```

### 2. Install dependencies

```bash
npm install
# or
yarn
```

### 3. Start the development server

```bash
npm run dev
# or
yarn dev
```

Open your browser:

```
http://localhost:3000
```

---

## 🌍 Supported Languages

| Language    | Code |
| ----------- | ---- |
| Azerbaijani | az   |
| English     | en   |

All translation files are located in:

```
/messages
```

---

## 🔗 Language-Based Routing

Pages are served based on the active language:

```
/az/about   → Azerbaijani
/en/about   → English
```

Each `[lang]/` folder renders pages for that specific locale.

---

## 🛠 Next Steps / Improvements

* Add more languages
* Integrate **Tailwind CSS** or other UI libraries
* Add **CMS support** (Sanity, Strapi, etc.) for dynamic content
* Improve **SEO and metadata handling**

---

## 📚 Resources / References

For a detailed guide on Next.js internationalization, see:
[Next.js i18n Tutorial](https://i18nexus.com/tutorials/nextjs/next-intl)

---

## ➕ Adding a New Language

1. **Update locales**
   Open `\i18n\routing.ts` and add your new language code:

   ```ts
   locales: ['en', 'az'], // => ['en', 'az', 'tr']
   ```

2. **Add a translation file**
   In the `/messages` folder, create a new JSON file for your language:

   ```text
   messages/
   ├─ az.json
   ├─ en.json
   └─ tr.json   <- New language
   ```

   Example `tr.json`:

   ```json
   {
     "hello": "Merhabalar"
   }
   ```

3. **Use translations in components**

   ```tsx
   import { useTranslation } from 'next-intl';

   const { t } = useTranslation('common');
   <h1>{t('hello')}</h1>
   ```

4. **Test your new language**
   Start the dev server and navigate to:

   ```
   /tr
   ```

Your app should now display Turkish translations.

---


