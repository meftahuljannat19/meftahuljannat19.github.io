# Meftahul Jannat — Portfolio

<p align="center">
  <a href="https://meftahuljannat.vercel.app">meftahuljannat.vercel.app</a>
</p>

A single-page personal portfolio for **Meftahul Jannat** — Lecturer in the Department of ICT at
Bangladesh Army University of Science and Technology (BAUST) and a Machine Learning researcher
working on computer vision, medical imaging, LLMs, bioinformatics and cyber security.

Built with plain **HTML, SCSS/CSS and vanilla JavaScript** — no framework, no build step
beyond compiling the SCSS.

---

## Sections

| Section | Content |
| --- | --- |
| **Home** | Name, role, and quick links to GitHub, email and Google Scholar. |
| **About** | Short bio, key figures (publications, research areas, CGPA), the undergraduate thesis cover linking to its published paper, and a **Download CV** button. |
| **Skills** | Four collapsible groups: AI & Machine Learning, Programming, Frameworks & tools, and Languages. |
| **Experience** | Two tabs — **Education** (B.Sc. at RUET, HSC, SSC) and **Work** (Lecturer at BAUST, Trainee Engineer at Ulkasemi, Research Assistant at AIMS Lab, UIU). |
| **Articles** | A Swiper carousel of the three published papers and two featured projects, each linking to its DOI or GitHub repository. |
| **Contact** | Location, GitHub handle, email, and a contact form. |

The site also ships a dark/light theme toggle (persisted in `localStorage`), a responsive
mobile navigation, scroll-spy navigation highlighting, and a scroll-to-top button.

---

## Publications featured

| Paper | Venue | DOI |
| --- | --- | --- |
| Real-time jute leaf disease classification using an explainable lightweight CNN via a supervised and semi-supervised self-training approach | Frontiers in Plant Science (2025) | [10.3389/fpls.2025.1647177](https://doi.org/10.3389/fpls.2025.1647177) |
| Lung Segmentation with Lightweight Convolutional Attention Residual U-Net | Diagnostics (2025) | [10.3390/diagnostics15070854](https://doi.org/10.3390/diagnostics15070854) |
| Cotton Leaf Disease (CLD) Classification Using Multihead External Attention Vision Transformer | 27th ICCIT (2024) | [10.1109/ICCIT64611.2024.11022519](https://doi.org/10.1109/ICCIT64611.2024.11022519) |

## Projects featured

- **[CXR-Agent](https://github.com/meftahuljannat19/cxr-agent)** — vision-language models
  (Llama-3.2-11B-Vision-Instruct, Qwen2-VL-7B-Instruct, finetuned with Unsloth) generating
  medical reports from chest X-rays on CheXpert and MIMIC.
- **[Automated Toll System](https://github.com/meftahuljannat19/Automated_Toll_System_YOLOv8)** —
  YOLOv8 vehicle detection on a custom 350-vehicle CVAT-annotated dataset plus EasyOCR number-plate
  recognition, driving a microcontroller-controlled toll gate.

---

## Project structure

```
.
├── assets/
│   ├── favicon/                  # favicons + web manifest
│   ├── MeftahulJannat-CV.pdf     # downloadable CV
│   └── meftahuljannat.vcf        # contact vCard
├── css/
│   ├── styles.css                # compiled from scss/styles.scss
│   └── swiper-bundle.min.css
├── img/
│   ├── profile.png               # hero portrait (transparent PNG, 500×500)
│   ├── thesis-cover.png          # About section visual
│   ├── article-1..3.png          # publication cards
│   └── project-1..2.png          # project cards
├── js/
│   ├── main.js                   # navigation, theme, tabs, swiper, contact form
│   └── swiper-bundle.js
├── scss/
│   ├── _variables.scss           # colors, typography, spacing tokens
│   └── styles.scss
├── index.html
├── robots.txt
└── sitemap.xml
```

## Running locally

No dependencies are required to view the site:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

To edit the styling, change the SCSS and recompile:

```bash
sass scss/styles.scss css/styles.css
```

---

## Configuration notes

- **Contact form.** `js/main.js` uses [EmailJS](https://dashboard.emailjs.com). Replace
  `EMAILJS_PUBLIC_KEY`, `EMAILJS_SERVICE_ID` and `EMAILJS_TEMPLATE_ID` at the bottom of the file
  with your own credentials. Until they are set, the form falls back to opening the visitor's
  mail client addressed to `CONTACT_EMAIL`.
- **Deployment URL.** `sitemap.xml`, `robots.txt` and `assets/meftahuljannat.vcf` assume
  `https://meftahuljannat.vercel.app/`. Update them if you deploy elsewhere.
- **LinkedIn.** The hero and footer link to GitHub and Google Scholar. Add a LinkedIn link in
  `index.html` once the profile URL is known.

---

## Credits

The design and original implementation of this template come from
[Judit Karamazov](https://github.com/JuditKaramazov). Distributed under the terms of the
included `LICENSE.txt`.

Content, imagery and copy © Meftahul Jannat.
