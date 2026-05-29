# Konnexu Block Template Guide

Follow this guide to format your community-submitted blocks and templates correctly.

---

## 📁 Repository Structure

Every new component must be placed inside its own folder within the `blocks/` directory using this exact structure:

blocks/
└── your-block-name/
    ├── README.md      (Setup instructions)
    ├── index.html     (HTML structure)
    └── style.css      (Optional custom CSS)

---

## 📄 1. The HTML Template (index.html)

Copy this starter code for your block structure. Use inline Tailwind utility classes whenever possible.

```html
<!-- 
  Konnexu Community Block: [Block Name]
  Author: [Your Name or GitHub Handle]
-->

<div class="konnexu-custom-block p-6 bg-white rounded-xl shadow-sm border border-gray-100">
  <h3 class="text-lg font-bold text-gray-900 mb-2">Block Title</h3>
  <p class="text-sm text-gray-600 mb-4">
    This is a standard template for a Konnexu community block.
  </p>
  
  <button class="konnexu-custom-btn px-4 py-2 text-white font-medium rounded-lg">
    Action Button
  </button>
</div>
```

---

## 🎨 2. The CSS Template (style.css - Optional)

Only include this file if your block requires styles beyond standard Tailwind. Always prefix your classes with `konnexu-` to prevent styling conflicts on live websites!

```css
/* 
  Custom Styles for: [Block Name]
*/

.konnexu-custom-block .konnexu-custom-btn {
  background: linear-gradient(135deg, #6366f1 0%, #4f46e5 100%);
  transition: transform 0.2s ease;
}

.konnexu-custom-block .konnexu-custom-btn:hover {
  transform: translateY(-1px);
}
```

---

## 📑 3. The Block Readme (README.md)

Every block needs a short description file so users know how to add it to their site. If you put the instructions/tutorial on the community,
please link that in your README file.

```markdown
# [Block Name]

A brief sentence explaining what this block does. If you put a tutorial at the community, please link it - no need for additional instructions.

## 🛠 Setup Instructions if not at the community (if at the community, please link the thread here)
1. Copy the code from `index.html`.
2. Go to your **Konnexu Admin Control Panel > Design & Navigation > Blocks**.
3. Create a new custom HTML block and paste the code.
4. *Optional:* Copy `style.css` into your theme's custom CSS settings.

```
