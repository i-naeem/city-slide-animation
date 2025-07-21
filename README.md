# 🌆 Swiper + GSAP Stack Slide Animation

This is a **custom animated Swiper slider** that uses **GSAP** (GreenSock) to achieve a **stack-like transition effect** for text and background. Designed for **modern websites** where visual storytelling or immersive section transitions are important — like portfolio sites, landing pages, or digital showcases.

---

## 🧠 What It Does

When you swipe or paginate through slides:

* The **city name text** animates like a stack:

  * The **current text** slides **downward and fades slightly**
  * The **next text** slides **from the top downward** into position
  * Both are visible during the transition — giving a **stack movement feel**
* The **background image** crossfades smoothly
* A **white transparent overlay** sweeps from **left to right**, adding visual polish

All three animations happen **simultaneously**, creating a clean, elegant transition.

---

## 🔧 Tech Stack

* [**Swiper.js**](https://swiperjs.com/) for slides/swiping/pagination
* [**GSAP (GreenSock)**](https://gsap.com/) for custom animation control
* [**Satoshi Font**](https://www.fontshare.com/fonts/satoshi) for modern typography
* Pure **HTML/CSS/JS** — no build tools or frameworks required

---

## 📂 Folder Structure

```
project/
│
├── index.html        # Full HTML with Swiper + GSAP animations
├── README.md         # This file
```

---

## 📦 Installation

No build tools needed. Just open `index.html` in a browser.

If integrating into your own website:

1. Copy the relevant `<link>`, `<style>`, and `<script>` sections
2. Ensure you include:

   * Swiper styles and JS
   * GSAP JS
   * Font from Fontshare (Satoshi)
3. Update your content, slide images, or city names as needed

---

## 🎬 How the Animation Works

### 1. **Text Stack Transition**

* Each slide contains `.slide-text` with the city name.
* On transition:

  * `prevText` is animated **down to `y: 100%`** and faded to opacity `0.2`
  * `nextText` is set at **`y: -100%`** initially, then animated **into `y: 0%`**
* Both animations happen **at the same time**, creating an overlapping moment where both texts are visible and look like stacked layers.

### 2. **Background Crossfade**

* Each `.background-img` fades out (`opacity: 0`) as the next one fades in (`opacity: 1`)
* This is synced with the text transitions

### 3. **Overlay Swipe**

* A `.overlay` with `rgba(255, 255, 255, 0.2)` slides from **left to right**
* It gives the feel of a **"light sweep"** across the slide

### 4. **Pagination**

* Swiper's default pagination bullets are styled and enabled
* Clicking them also triggers the animation sequence

---

## 🛠 Customization Guide

| Task                        | How to Do It                                         |
| --------------------------- | ---------------------------------------------------- |
| Change transition **speed** | Update `speed` in Swiper config (e.g. `speed: 2000`) |
| Adjust **text size**        | Change `font-size` of `.slide-text` (e.g. `8rem`)    |
| Modify **fade duration**    | Edit GSAP `duration` values in `.to()` calls         |
| Change **city names**       | Update the `.slide-text` content                     |
| Add more **slides**         | Duplicate `.swiper-slide` with new image/text        |
| Change **easing style**     | Use GSAP easing like `"power2.out"`, `"expo.in"`     |
| Use **autoplay**            | Add `autoplay: { delay: 5000 }` to Swiper config     |
| Use **custom arrows**       | Add `navigation: { nextEl, prevEl }` in Swiper       |
| Fade **only half** of text  | Mask text with `linear-gradient()`                   |

---

## 💡 Example Use Cases

* Hero section of a homepage (e.g., "Explore Tokyo, New York, Osaka")
* Full-screen city/gallery/showcase slider
* Digital storytelling sections
* Intro animations for creative agencies

---

## 📸 Images Used (Unsplash)

* [Image 1](https://plus.unsplash.com/premium_photo-1680582107403-04dfac02efc3)
* [Image 2](https://plus.unsplash.com/premium_photo-1683888229109-17cb0975af20)
* [Image 3](https://plus.unsplash.com/premium_photo-1682048358672-1c5c6c9ed2ae)

Feel free to replace these with your own.

---

## 🧪 Testing & Performance

* Fully responsive on desktop and mobile
* Smooth 60fps animation with GSAP
* Touch-enabled swipe (thanks to Swiper)
* Tested in Chrome, Firefox, Safari

---

## ✅ Final Notes

This slider is built to feel **high-end and modern**, combining Swiper's robust core with **GSAP's fine-grained animation control**. It goes beyond simple fade or slide — offering a **cinematic transition experience** suitable for high-visual websites.
