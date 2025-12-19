# **Wasker \- Personal Portfolio/Resume Static Website Template**

**Wasker** is a beautifully designed and smoothly interactive personal portfolio and resume website template. It is crafted for designers, developers, or freelancers to showcase their skills, project experience, and blog posts.

Built with native HTML/JS, it integrates modern frontend libraries to deliver a seamless **Single Page Application (SPA)** experience without the complexity of a full framework.

## **✨ Key Features**

* **Seamless Page Transitions (SPA Experience)**: Powered by [Swup.js](https://swup.js.org/), links do not trigger a full page reload, providing a smooth, app-like transition experience.  
* **High-Performance Animations**: Integrated with [GSAP](https://greensock.com/gsap/) (GreenSock) and ScrollTrigger to create complex parallax effects and element entrance animations.  
* **Responsive Layout**: Built on the Bootstrap Grid system, ensuring perfect adaptation across mobile, tablet, and desktop devices.  
* **Portfolio Filtering**: Uses [Isotope](https://isotope.metafizzy.co/) for category filtering and masonry layouts.  
* **Lightbox Gallery**: Integrated with [Fancybox](https://fancyapps.com/fancybox/) for immersive image and video previews.  
* **Touch Sliders**: Uses [Swiper](https://swiperjs.com/) for touch-friendly carousels (e.g., Testimonials, Services).  
* **Dark Mode Design**: A carefully crafted dark UI style that highlights professionalism.

## **🛠 Tech Stack**

* **Core**: HTML5, CSS3, JavaScript (ES6)  
* **Styling**: Bootstrap Grid (Grid system only), FontAwesome 5 Pro (Icons)  
* **Key Plugins**:  
  * swup.js (Page routing/transitions)  
  * gsap.js (Animation engine)  
  * swiper.js (Slider component)  
  * fancybox.js (Lightbox/Modal)  
  * isotope.js (Layout sorting & filtering)  
  * smooth-scroll.js (Smooth scrolling behavior)

## **📂 Directory Structure**
```
Wasker/  
├── assets/                 \# Static Resources  
│   ├── css/                \# Stylesheets  
│   │   ├── style.css       \# Main stylesheet  
│   │   └── plugins/        \# 3rd party CSS (bootstrap-grid, fancybox, swiper, etc.)  
│   ├── js/                 \# Scripts  
│   │   ├── main.js         \# Core logic (Plugin init, Animation config)  
│   │   └── plugins/        \# 3rd party JS  
│   ├── img-dark/           \# Images (Avatar, Portfolio thumbnails, Backgrounds)  
│   ├── fonts/              \# Font icon files  
│   └── files/              \# Downloadable files (e.g., CV PDFs)  
├── blog/                   \# Blog Module  
│   ├── index.html          \# Blog list page  
│   └── publication.html    \# Blog post detail page  
├── contact/                \# Contact Module  
│   └── index.html          \# Contact page  
├── portfolio/              \# Portfolio Module  
│   ├── index.html          \# Portfolio list page  
│   └── project.html        \# Project detail page  
└── index.html              \# Homepage (Resume/Main)
```
## **🚀 Quick Start**

Since the project uses swup.js (which involves AJAX requests) and ES Modules, **you cannot open index.html directly via double-click**. Doing so will result in Cross-Origin (CORS) errors or broken navigation. **You must run it on a local server.**

### **Method 1: Using VS Code (Recommended)**

1. Open the project folder in VS Code.  
2. Install the **Live Server** extension.  
3. Right-click index.html and select **"Open with Live Server"**.

### **Method 2: Using Python**

If you have Python installed, run the following command in the project root:

```Bash
\# Python 3.x  
python \-m http.server 8000
```
Then visit http://localhost:8000 in your browser.

### **Method 3: Using Node.js**

If you have Node.js installed:

```Bash
\# Install http-server globally  
npm install \-g http-server

\# Run in project root  
http-server .
```
## **⚙️ Customization Guide**

1. **Personal Information**: Open index.html and search for keywords like "Walter Archer" or "UI/UX Design" to replace them with your own text.  
2. **Images**:  
   * **Avatar**: Replace assets/img-dark/ui/avatar.jpg.  
   * **Portfolio**: Replace images inside the assets/img-dark/portfolio/ directory.  
3. **Menu Configuration**: The navigation bar is located in the .mil-menu-part section of every HTML file.  
4. **Animation Tweak**: Animation logic is centralized in assets/js/main.js. Search for gsap keywords to adjust animation parameters.

## **⚠️ Migration Notes (Vue.js)**

If you plan to migrate this project to Vue.js:

* **Remove Swup**: Vue Router handles routing natively; swup.js is not needed.  
* **Lifecycle Hooks**: Initialization code in main.js (like Isotope or Swiper) should be moved to the Vue onMounted lifecycle hook.  
* **DOM Manipulation**: Use Vue ref to access elements instead of document.querySelector.

## **📄 Credits & License**

* **Design Reference**: [Nazar Miller](https://www.bootstrapmb.com)  
* **Usage**: This project is for educational and personal use.
