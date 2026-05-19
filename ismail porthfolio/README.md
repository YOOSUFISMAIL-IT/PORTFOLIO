# ISMAIL – Personal Portfolio Website

[![Live Demo](#)](https://your-demo-link.com)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
<img width="1025" height="860" alt="Screenshot 2026-05-19 102948" src="https://github.com/user-attachments/assets/74bf6956-d2d5-4725-9676-812b52540ffa" />



A modern, responsive personal portfolio website for **Yoosuf Mohamed Ismail** – an aspiring IT professional, full‑stack developer, and tech enthusiast. Built with pure HTML, CSS, and JavaScript.

![Portfolio Screenshot](images/screenshot.png)  
*(Add a screenshot of your site in the `images` folder and update the path)*

---

## 🚀 Features

- **Fully responsive** – works on desktop, tablet, and mobile.
- **Dynamic skill bars** – animate when scrolled into view.
- **Certification gallery** – view certificates (images/PDFs) in a modal lightbox.
- **Contact form** – client‑side validation with demo alert (ready to connect to a backend).
- **Smooth scrolling** and active navigation highlighting.
- **Social links** – Facebook, GitHub, Instagram, LinkedIn.
- **Downloadable CV** button linked to Google Drive.
- **Read more / read less** toggle for the About section.

---

## 🛠️ Technologies Used

| Category       | Technologies                                                                 |
|----------------|------------------------------------------------------------------------------|
| Frontend       | HTML5, CSS3, JavaScript (ES6)                                               |
| Icons          | Font Awesome 6                                                              |
| Fonts          | Google Fonts – Anta                                                         |
| Deployment     | GitHub Pages / any static host                                              |

---

## 📁 Folder Structure

Replace content
Profile picture – update images/img1.jpg (used in home & about sections).

Project images – replace images/ima3.png, img4.png, or the placeholder https://placehold.co/... in the portfolio section.

Certificates – put your certificate images/PDFs inside images/ and update the src attributes in the certification items (search for img6.pdf, img22.pdf, etc.).

Social links – change the href in .social-media a and .social-icons a to your real profiles.

CV link – replace the Google Drive URL in the “Download CV” button.

Contact info – update phone, email, and address in the footer.


:root {
  --bg-color: #1f242e;
  --main-color: #0ef;
  /* change these to your brand colours */
}


Contact Form


The form currently shows a demo alert on submit. To make it functional, you can:

Use a backend service like Formspree, EmailJS, or Netlify Forms.

Or connect to your own server endpoint by modifying the fetch inside the submit event listener.

Example (using Formspree):
fetch('https://formspree.io/f/your-endpoint', {
  method: 'POST',
  body: new FormData(contactForm)
})

 Future Improvements
Add a dark/light theme switcher.

Convert skills data into a JSON file for easier updates.

Add a working blog section.

Integrate a real‑time chat widget.

 License
This project is open source and available under the MIT License.


 Author
Yoosuf Mohamed Ismail





