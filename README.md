# ✨ Alexos - Connect, Share, and Vibe

**Alexos** is a modern, fully client-side social networking and messaging web application. Inspired by platforms like Facebook and Messenger, it features a sleek UI, dynamic theming, and a unique "Vibe" system for posts. 

*Crafted with ❤️ by Lwandile.*

## 🚀 Features

### 🔐 Authentication & Profiles
- **Multi-User Support:** Fully functional Sign Up and Log In system.
- **Auto-Generated Avatars:** Unique, stylish avatars for every user powered by the DiceBear API.
- **User Profiles:** Dedicated profile view with custom bios.

### 📱 Social Feed
- **The "Vibe" System:** Attach a mood (🌊 Chill, 🔥 Hype, 🌿 Nature, 🌙 Night) to your posts, which dynamically changes the post's aesthetic border and glow.
- **Smart Image Uploads:** Upload real photos from your device. The app automatically compresses and resizes them using HTML5 Canvas to prevent LocalStorage overflow.
- **Rich Interactions:** Auto-expanding text areas and smooth pop-in animations.

### 💬 Real-Time Messaging (Inbox)
- **Messenger-Style Chat:** A full-featured inbox with contact lists, unread badges, and chat bubbles.
- **Cross-Tab Synchronization:** Uses the browser's native `localStorage` events to sync messages in real-time across different browser tabs without needing a backend server!

### 🎨 Modern UI/UX
- **Dark & Light Themes:** Beautifully designed dark mode (default) and light mode with a seamless toggle.
- **Glassmorphism & Animations:** Smooth transitions, hover effects, and modern card-based layouts.
- **Fully Responsive:** Adapts gracefully to mobile and desktop screens.

## 🛠️ Tech Stack

- **Frontend:** Pure HTML5, CSS3 (with CSS Variables for theming), Vanilla JavaScript (ES6+).
- **Storage:** Browser `localStorage` (acting as a lightweight client-side database).
- **External APIs:** [DiceBear](https://dicebear.com/) for SVG avatar generation.
- **Backend:** None! 100% client-side.

## 📦 Getting Started

Since Alexos is a purely client-side application, there is no complex setup or installation required.

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge).

## 🧪 How to Test Multi-User & Real-Time Messaging

Because Alexos doesn't use a backend server, the "real-time" messaging works by syncing `localStorage` events across open browser tabs. Here is how to test it:

1. **Open Tab 1:** Open `index.html` in your browser. Sign up as **User A** (e.g., username: `lwandile`).
2. **Open Tab 2:** Open `index.html` in a **new tab** or an **Incognito/Private window**. Sign up as **User B** (e.g., username: `alexos`).
3. **Send a Message:** In Tab 1, go to the Inbox (💬), click on User B, and type a message.
4. **Watch the Magic:** Look at Tab 2. The message will appear instantly, and the unread badge will update without you having to refresh the page!

---

## 🏗️ Architecture Note

**How does real-time messaging work without a backend?**
Alexos leverages the browser's native `window.addEventListener('storage', ...)` event. When Tab 1 writes a new message to `localStorage`, the browser automatically fires a `storage` event in Tab 2. Tab 2 listens for this event, reads the new data, and updates the UI instantly. 

*Note: Because it relies on `localStorage`, data is isolated to the specific browser and device. Clearing browser data will reset the app.*

---

## To use the app

