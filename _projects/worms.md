---
layout: portfolio_page
title: WORMS Lunar Robot
date_range: "Nov 2021 – Apr 2022" # junior fall - senior fall
end_date: 2023-04-15  
tags: [testing]
cover_image: /assets/images/portfoliotiles/wormstile.png
---

<div class="project-detail">
  <h1 class="project-title">{{ page.title }}</h1>
  <p class="project-dates">{{ page.date_range }}</p>

<div class="project-section">

  <!-- Intro Section -->
  <div class="project-intro">
    <p>
      <b>WORMS (Walking Oligomeric Robotic Mobility System)</b> refers to an architecture for a robotic mobility system to access extreme lunar terrain. The name emerges from the integration of a small (‘oligomeric’) set of nearly-identical, articulating ‘worms’ to create a diverse set of robots. Mimicking arms, legs and backbones, WORMS can be configured into diverse walking robots with payload capacity from kilograms to tons.  Together with a small set of simple Accessories, such as different types of shoes or pallets / chassis, the architecture can be assembled into larger robot configurations tailored to the needs of various extreme terrain access missions. Each Worm or Accessory can optionally be enhanced with added functionality defined by interchangeable Species Modules. These could include a LIDAR unit, an anchoring drill, a winch, an additional battery and many more tools or sensors. The key idea is that all elements of WORMS can be easily reconfigured in the field by non-specialists to accomplish a large variety of mobility missions, including but not limited to extreme terrain access (<a href="https://spaceresources.mit.edu/worms-2022/" target="_blank" rel="noopener">WORMS website</a>).
    </p>
    <p>
      The WORMS team received $174,000 in funding from the NASA BIG Idea Challenge in 2022 and has since built and tested a prototype with 6 articulating "worms" for legs, a body chassis, and a "Navigator" module. The team presented at the BIG Idea Challenge and has participated in several conferences and competitions.
    </p>
    <!-- Awards -->
    <div>
      <h3>Awards & Recognition</h3>
      <ul>
        <li>IEEE Aerospace Conference - Charles M. Fogg Best Paper Award (2023)</li>
        <li>2nd place at MassRobotics Form & Function Challenge (2023)</li>
        <li>Best Technical Paper at NASA's BIG Idea Presentation (2022)</li>
      </ul>
    </div>
  </div>

  <div class="video-grid">
    <div class="video-container-worms">
      <div class="video-wrapper">
        <iframe src="https://www.youtube.com/embed/5B2cSCKrPTE?si=nIzVTudB0r7BbaAu" title="Video 1" frameborder="0" allowfullscreen></iframe>
      </div>
      <p class="video-caption-worms">Project Proposal</p>
    </div>
    <div class="video-container-worms">
      <div class="video-wrapper">
        <iframe src="https://www.youtube.com/embed/U72lmSXEVkM?si=qdPgQ-bhxg6v5aFx" title="Video 2" frameborder="0" allowfullscreen></iframe>
      </div>
      <p class="video-caption-worms">Project Summary</p>
    </div>
  </div>

<div class="pdf-row">
  <div class="pdf-card">
    <div class="pdf-preview-wrapper">
      <embed src="/assets/pdfs/worms_content/BIG_Idea_Paper_2022.pdf" type="application/pdf" class="pdf-preview">
      <button class="fullscreen-btn" onclick="openInNewTab(this)">Open in New Tab</button>
    </div>
    <p class="pdf-caption">BIG Idea Paper 2022</p>
  </div>

  <div class="pdf-card">
    <div class="pdf-preview-wrapper">
      <embed src="/assets/pdfs/worms_content/Ascend_WORMS_2022.pdf" type="application/pdf" class="pdf-preview">
      <button class="fullscreen-btn" onclick="openInNewTab(this)">Open in New Tab</button>
    </div>
    <p class="pdf-caption">Ascend Paper 2022</p>
  </div>

  <div class="pdf-card">
    <div class="pdf-preview-wrapper">
      <embed src="/assets/pdfs/worms_content/IEEE_Aerospace_2023.pdf" type="application/pdf" class="pdf-preview">
      <button class="fullscreen-btn" onclick="openInNewTab(this)">Open in New Tab</button>
    </div>
    <p class="pdf-caption">IEEE Aerospace Paper 2023</p>
  </div>
</div>

  <hr class="carousel-separator">


  <!-- Section 1 -->
  <div class="project-section" >
    <h3 style="font-size: 20px; font-weight: bold;">Early Concept Development</h3>
    <p>
      I was one of seven team members who launched the concept of WORMS. We spent several months brainstorming solutions for the extreme lunar terrain mobility challenge proposed by NASA. We designed a modular architecture and selected a hexapod configuration for the demonstration. Once the concept was solidified, I took the lead on developing initial ideas for two key components:
    </p>
    <ul>
      <li><b>Specialized Shoes for Lunar Regolith</b> – Designed to minimize sinking in high-porosity lunar regolith.</li>
      <li><b>Robot Chassis</b> – Designated as the attachment point for the legs and used to support payload.</li>
    </ul>
    <p>
      In addition, I conducted literature review to inform design decisions, defined system-level requirements, identified risks, and created test plans.
    </p>
    <div class = "image-row-worms2">
      <img src="/assets/images/worms_content/WORMS_team1.jpeg" alt="Concept Image 1" style="width: 50%;">
      <img src="/assets/images/worms_content/WORMS_team2.jpeg" alt="Concept Image 2" style="width: 50%;">
    </div>
  </div>

  <!-- Section 2 -->
  <div class="project-section" style="margin-bottom: 50px;">
    <h3 style="font-size: 20px; font-weight: bold;">Body Chassis/Pallet Design</h3>
    <p>
      As part of the Accessories Team, I collaborated on the design of the hexapod body chassis. Before the summer build phase, I created an initial version of the pallet, which the summer team iterated into the final 2-layered design which had further mass reduction and integrated attachment points for the legs. Key constraints included:
    </p>
    <p>
      <b>Mass limit:</b> ≤ 10 kg<br>
      <b>Load capacity:</b> Pallet is strong enough to handle leg loads during walking when middle two legs (3, 6) are lifted simeltaneously and when diagonally located legs (2, 5) are lifted simeltaneously.<br>
      <b>Interface:</b> Universal Interface Blocks (UIBs) - the common mating adapter for all mechanical, electrical and data connections between Worms, Accessories and Species Modules - are positioned to avoid leg collisions.
    </p>
    <div style="display: flex; justify-content: center; align-items: flex-start; gap: 20px; margin-top: 20px;">
      <figure style="flex: 0 0 auto; text-align: center; margin: 0;">
        <img src="/assets/images/worms_content/init_pallet.png" alt="Initial Pallet" style="max-height: 280px; width: auto; display: block; border-radius: 4px;">
        <figcaption style="margin-top: 4px; font-size: 0.9em; color: #555;">Initial Pallet</figcaption>
      </figure>
      <figure style="flex: 0 0 auto; text-align: center; margin: 0;">
        <img src="/assets/images/worms_content/final_pallet.png" alt="Final Pallet" style="max-height: 280px; width: auto; display: block; border-radius: 4px;">
        <figcaption style="margin-top: 4px; font-size: 0.9em; color: #555;">Final Pallet</figcaption>
      </figure>
    </div>



  </div>

  <!-- Section 3 -->
  <div class="project-section" style="margin-bottom: 50px;">
    <h3 style="font-size: 22px; font-weight: bold;">Shoe Design for Lunar Terrain</h3>
    <p>
      The WORMS shoes are modular accessories designed for different terrains. For this prototype, we targeted high-porosity regolith and used artificial snow as a regolith simulant. I developed and tested two prototypes:
    </p>
    <p><b>Prototype 1: </b>Flat, layered design to maximize surface area and reduce mass.</p>
    <p><b>Prototype 2: </b>Bowl design, inspired by Apollo Lander's footpads, for stability and load distribution.</p>
    <p>
    The flat shoe sank the least under a 14 kg load on artificial snow. However, the rounded shoe shape provides better contact and stability on rocky surfaces, while allowing tip/tilt motion when traversing uneven terrain. Our final design used repurposed stainless-steel woks, which are shallower at the bottom and gradually round toward the top - a compromise between flat and curved geometries. An acrylic insert was added inside to provide a flat surface for UIB mounting.
    </p>
    <div style="display: flex; justify-content: center; align-items: flex-start; gap: 10px; margin-top: 20px;">
      <figure style="flex: 1.5; text-align: center; margin: 0;">
        <img src="/assets/images/worms_content/flatshoe.jpg" alt="Shoe Prototype 1" style="width: 100%; height: auto; border-radius: 2px; display: block;">
        <figcaption style="margin-top: 4px; font-size: 0.9em; color: #555;">Shoe Prototype 1</figcaption>
      </figure>
      <figure style="flex: 1.5; text-align: center; margin: 0;">
        <img src="/assets/images/worms_content/wokshoe.jpg" alt="Shoe Prototype 2" style="width: 100%; height: auto; border-radius: 2px; display: block;">
        <figcaption style="margin-top: 4px; font-size: 0.9em; color: #555;">Shoe Prototype 2</figcaption>
      </figure>
      <figure style="flex: 0.85; text-align: center; margin: 0;">
        <img src="/assets/images/worms_content/finalshoe.jpg" alt="Final Shoe" style="width: 100%; height: auto; border-radius: 2px; display: block;">
        <figcaption style="margin-top: 4px; font-size: 0.9em; color: #555;">Final Shoe</figcaption>
      </figure>
    </div>
  </div>

  <div class="project-section" style="margin-bottom: 50px;">
    <h3 style="font-size: 20px; font-weight: bold;">Testing & Validation</h3>
    <p>
      After the prototype had been built, bi-weekly testing sessions were scheduled and organized to test each unit, each subsystem, and finally the whole system together.
    </p>
    <div style="margin-top: 20px; text-align: center;">
      <video controls style="width: 80%; max-width: 800px; border-radius: 2px;">
        <source src="/assets/videos/WORMSdemo.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </div>






</div>




<script>
function openInNewTab(button) {
  const embed = button.closest('.pdf-card').querySelector('embed');
  if (embed) {
    const pdfSrc = embed.getAttribute('src');
    if (pdfSrc) {
      window.open(pdfSrc, '_blank');
    } else {
      console.error("No PDF src found on embed.");
    }
  } else {
    console.error("No embed element found.");
  }
}
</script>