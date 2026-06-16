# Konnexu Block Template Guide

Follow this guide to format your community-submitted blocks and templates correctly. Please include a link to the full tutorial that is posted
at our community.

---

## 📁 Repository Structure

Place every new component inside its own folder within the `blocks/` directory using this layout:

```text
blocks/
└── your-block-name/
    ├── README.md      (Setup instructions)
    ├── index.html     (HTML structure)
    └── style.css      (Optional custom CSS)
```

---

## 📄 1. The HTML Template (index.html)

Copy this starter code for your block structure. Use inline Tailwind utility classes whenever possible.

```html
<!-- 
  Konnexu Community Block: [Insert Block Name Here]
  Author: [Your Name or GitHub Username]
  Tutorial: [Paste Community Thread URL Here]
-->

<!-- Main Wrapper: Use unique custom classes combined with utility classes -->
<div class="konnexu-custom-block p-6 bg-white rounded-xl shadow-sm border border-gray-100" role="region" aria-label="[Briefly describe block purpose]">

	<!-- 1. Header Section -->
	<h3 class="text-lg font-bold text-gray-900 mb-2">
		[Block Title]
	</h3>

	<!-- 2. Content Body -->
	<p class="text-sm text-gray-600 mb-4">
		This is a standard boilerplate template for a Konnexu community component. Replace this text with your custom block content.
	</p>

	<!-- 3. Action Elements -->
	<button type="button" class="konnexu-custom-btn px-4 py-2 text-white font-medium rounded-lg">
		[Action Button]
	</button>

</div>
```

---

## 🎨 2. The CSS Template
If posting CSS customizations, temp fixes, or other issues just for CSS, please name your CSS file for what it does. For example, we have a 
fix for the photo view background and named it "photoviewbg.css". Have a look at that file for how we formatted the tips/example code.

If you're doing a tutorial for a block that requires styles beyond standard Tailwind, always prefix your classes with `konnexu-` to prevent styling 
conflicts on live websites!

Please use the following example of how to format your CSS file. You can also look at other CSS files in our repo.

```css
/**
 * Konnexu Community Block Stylesheet: [Insert Block Name Here]
 * Author: [Your Name or GitHub Username]
 * Tutorial: [Paste Community Thread URL Here]
 */

/* ==========================================================================
   1. Component Variables & Tokens
   ========================================================================== */
/* Define component-specific colors, spacing, or animation configurations here */
:root {
    --konnexu-[block-name]-bg: #ffffff;
    --konnexu-[block-name]-text: #111827;
    --konnexu-[block-name]-accent: #3b82f6;
}

/* ==========================================================================
   2. Main Container / Wrapper Styling
   ========================================================================== */
/* Apply styling to the root container of your block */
.konnexu-custom-block {
    background-color: var(--konnexu-[block-name]-bg);
    color: var(--konnexu-[block-name]-text);
    /* Add custom layout properties below if not handled by utility classes */
}

/* ==========================================================================
   3. Inner Elements & Typography
   ========================================================================== */
/* Style internal headings, paragraphs, and list items safely */
.konnexu-custom-block h3 {
    /* Custom font treatments or spacing overrides */
}

.konnexu-custom-block p {
    /* Body copy line-height or text treatments */
}

/* ==========================================================================
   4. Interactive Elements & Actions
   ========================================================================== */
/* Style buttons, links, forms, and their respective interactive states */
.konnexu-custom-btn {
    background-color: var(--konnexu-[block-name]-accent);
    transition: background-color 0.2s ease-in-out, transform 0.1s ease;
}

.konnexu-custom-btn:hover {
    filter: brightness(90%);
}

.konnexu-custom-btn:active {
    transform: scale(0.98);
}

/* ==========================================================================
   5. Responsive / Theme Overrides (Optional)
   ========================================================================== */
/* Place your dark mode preferences or responsive media queries here */
@media (prefers-color-scheme: dark) {
    /* Define dark theme variations if required by the core setup */
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
