---
layout: portfolio_page
title: PEARL Autonomous Floating Robot
date_range: "Jan 2021 – Dec 2021" # soph iap - junior fall
end_date: 2021-12-15  
tags: [testing]
cover_image: /assets/images/portfoliotiles/pearltile.gif
---

<div class="project-detail">
  <h1 class="project-title">{{ page.title }}</h1>
  <p class="project-dates">{{ page.date_range }}</p>
  <div class="project-section">
        <p><b>PEARL (Platform for Expanding AUV exploRation to Longer ranges)</b> is a concept for an autonomous floating servicing platform that can harvest solar energy to recharge autonomous underwater vehicles (AUVs) and connect to new generation high-bandwidth low-Earth orbit (LEO) satellite constellations for near-real-time data transmission. You can read more about PEARL <a href="https://followpearl.mit.edu/" target="_blank" rel="noopener">here</a> .
    </p>
    <p>
    I worked on PEARL as an undergraduate researcher in the Engineering Systems Lab. I started off performing hydrodynamic analysis on PEARL for design verification. During the summer I worked on several projects as a full-time researcher on PEARL:</p>
    <ul>
      <li>Lead the PEARL team to rebuild and deploy PEARL A and manufacture, build, and deploy PEARL B.</li> 
      <li>Designed and built an autonomous anchoring module to enable PEARL to maintain position during missions.</li>
      <li>Designed and machined a custom maintenance platform to improve accessibility to PEARL’s electronics.</li>
      <li>Led testing and integration of a hydrophone system to capture acoustic data, and developed initial methods for signal analysis.</li>
    </ul>
    <p>
      During the subsequent fall semester I worked further on analyzing hydrophone data via a class called Measurement and Instrumentation (2.671).
    </p>
    <p>
    We also submitted this work to the MIT Mechanical Engineering De Florez Competition and won 2nd place!
    </p>
  </div>

  <div class="image-carousel-container">
    <h2 class="carousel-title">Hydrodynamic Analysis</h2>
    <p class="carousel-subtitle">(Analyzing PEARL's response to the ocean environment through simulation.)</p>
    <div class="image-carousel" id="carousel-hydrodynamics">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/oceanwavespectrum.png" alt="Ocean Waves Spectrum" style="width: 80%;">
        <div class="caption"><b>Ocean Waves Frequency Spectrum.</b> Distribution of energy among different wave frequencies in a "fully developed sea" according to the Pierson-Moskowitz spectrum. Ocean wave frequencies are mostly between 0.04-0.15 Hz</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/pearlmesh.png" alt="PEARL Mesh" style="width: 100%;">
        <div class="caption"><b>PEARL simplified mesh.</b> A simplified PEARL CAD imported from Fusion 360 and viewed in Capytaine's visual interface. Capytaine is a Python library used to simulate the interaction between water waves and floating bodies in the frequency domain. </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/heaveaddedmass.png" alt="Heave Added Mass" style="width: 70%;">
        <div class="caption"><b>PEARL Heave Added Mass.</b> Added mass refers to the inertia added to a system because an accelerating or decelerating body must move (or deflect) some volume of surrounding fluid as it moves through it (<a href="https://en.wikipedia.org/wiki/Added_mass" target="_blank" rel="noopener">Wikipedia</a>). Heave refers to the up and down movement of a structure in a fluid. The plate at the base of PEARL is used to reduce the heave motion by increasing the heave added mass, which increases stability.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/pearlrao.png" alt="Heave RAO" style="width: 60%;">
        <div class="caption"><b>PEARL Heave RAO.</b> The Response Amplitude Operator (RAO) tells us the response of a body in the given direction at different frequencies. If RAO < 1, the body's motion is damped compared to the amplitude of the incoming wave. This plot shows that the body does not resonate in the heave direction at the frequencies that are prominent in the ocean (according to Pierson-Moskowitz).</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-hydrodynamics', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-hydrodynamics', 1)">&#10095;</button>
  </div>

    <hr class="carousel-separator">


  <div class="image-carousel-container">
    <h2 class="carousel-title">PEARL Fabrication, Assembly, and Deployment</h2>
    <p class="carousel-subtitle">(Building and deploying PEARL A and B in Pleasant Bay and the Charles River.)</p>
    <div class="image-carousel" id="carousel-build">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/Pearl_CAD.jpg" alt="Pearl CAD" style="width: 80%;">
        <div class="caption"><b>PEARL CAD.</b></div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/PearlAbuild.jpg" alt="PEARL A Build Day" style="width: 80%;">
        <div class="caption"><b>PEARL A Redeployment.</b> This was build day for PEARL A, which was to be deployed at Pleasant Bay. Prior to build day, I had machined and procured replacement parts, and we had readied the pontoons and damping plate. It took 5 of us 7 hours to completely re-build PEARL's frame as many of the bolts had been rusted or stripped.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/machining.png" alt="Machining Parts" style="width: 80%;">
        <div class="caption"> <b>PEARL B Fabrication.</b> I waterjet angle brackets out of 1/8" aluminium (top left), waterjetted motor mounts from 1" aluminium and drilled/tapped the holes (right), and vertical sawed/milled a large amount of 80/20 to precise lengths for PEARL's frame. The giant calipers (bottom left) were used to measure the pieces of 80/20 :). </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/PearlBDay1.jpg" alt="PEARL B Build Day 1" style="width: 80%;">
        <div class="caption"><b> PEARL B Build Day 1.</b> PEARL B was planned to be deployed to the Charles River from the MIT Sailing Pavilion. We put together sub-assemblies for PEARL's structure in the machine shop and carted them over to the Sailing Pavilion for further assembly.
        </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/PearlBDay2.jpeg" alt="PEARL B Build Day 2" style="width: 80%;">
        <div class="caption"><b> PEARL B Build Day 2.</b> We finished mechanical assembly with the whole team, adding on the solar panels last. We also assembled the electronics, including 2 Raspberry Pi's, an Arduino, a Power Distribution Board (PDB) and associated harnessing with waterproof connectors, in the black pelican box.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/PearlB.jpeg" alt="Completed PEARL B" style="width: 80%;">
        <div class="caption"><b>Completed PEARL B.</b> PEARL B stays on the side of the Sailing Pavilion for the most part and we take her out for testing and experiments when needed!</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-build', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-build', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

  <div class="image-carousel-container">
    <h2 class="carousel-title">Autonomous Anchor Module</h2>
    <p class="carousel-subtitle">(Designing and building an anchoring module for PEARL’s autonomous missions.)</p>
    <div class="image-carousel" id="carousel-anchor">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/air_anchor_test.gif" alt="Anchor Test" style="width: 60%;">
        <div class="caption"><b>Autonomous Anchor Test.</b> A hall effect sensor and magnet are placed strategically on the davit to sense when the anchor is up. This was a successful test where the sensing method restricted the winch from reeling the anchor in further once the anchor was fully seated in the davit</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/pool_anchor_test.gif" alt="Pool Anchor Test" style="width: 60%;">
        <div class="caption"><b>Autonomous Anchor Pool Test.</b> A proof of operation test is sucessfully run in the pool before attaching the module to PEARL.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/anchorsystem.png" alt="Anchor System Diagram" style="width: 70%;">
        <div class="caption"><b>Design Details of Anchor Module. </b>(b) The control circuit connects the hall effect sensor to an Arduino. The winch motor is driven by a motor controller connected to the Arduino. (c) The davit (anchor roller) with the integrated hall effect sensor and magnet.(d) The SLA-printed housing for the sensor, fabricated on a Formlabs printer. The sensor and housing are coated with epoxy for waterproofing.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/pearl_anchor_test.gif" alt="Anchor Test PEARL" style="width: 60%;">
        <div class="caption"><b>Anchor Test on PEARL. </b> A proof of operation test on PEARL was also successful!</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/anchor_assembly.jpg" alt="Anchor Assembly" style="width: 60%;">
        <div class="caption"><b>Attaching Anchor Module to PEARL.</b></div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/anchoronpearl.jpg" alt="Completed Assembly" style="width: 60%;">
        <div class="caption"><b>Completed Assembly!</b></div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-anchor', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-anchor', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

<div class="image-carousel-container">
    <h2 class="carousel-title">Hydrophone Integration and Analysis</h2>
    <p class="carousel-subtitle">(Adding underwater sound sensing to monitor boat traffic.)</p>
    <div class="image-carousel" id="carousel-hydrophone">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/hydrophone_schematic.png" alt="Hydrophone Schematic" style="width: 80%;">
        <div class="caption"><b>Hydrophone Setup.</b> A hydrophone is used to capture audio underwater. I selected the H2A hydrophone as a low-cost option for initial testing and integrated it with a Raspberry Pi. I then developed shell scripts for configuration and automatic recording.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/pool_hydrophone_test.png" alt="Hydrophone Validation" style="width: 100%;">
        <div class="caption"><b>Hydrophone Validation.</b> Tested hydrophone audio capture with controlled frequencies emitted by an iPhone. Verified that the emitted 1000Hz tone was present in the frequency spectrum of the audio capture.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/FFTs_capecod_motorboats.png" alt="Measuring Motorboat Speed via Hydrophone" style="width: 70%;">
        <div class="caption"><b>Motorboat Speed Sensing.</b> By the Doppler Effect, we know that a moving sound source is perceived as a frequency shift by a stationary observer. Using the hydrophone, we recorded motorboats passing at different speeds, and the frequency spectrum revealed clear shifts at higher speeds. This initial experiment, was used as inspiration for further analysis conducted for my Measurement and Instrumentation class project. </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/capecod_hydrophone_test.jpg" alt="Field Testing" style="width: 60%;">
        <div class="caption"><b>Hydrophone Field Testing!</b></div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-hydrophone', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-hydrophone', 1)">&#10095;</button>
  </div>

<hr class="carousel-separator">

<div class="image-carousel-container">
    <h2 class="carousel-title">Maintenance Platform</h2>
    <p class="carousel-subtitle">(Designing and fabricating a platform to make electronics maintenance more accessible.)</p>
    <div class="image-carousel" id="carousel-maintenance">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/before_platform.jpeg" alt="Pre-Maintenance Platform" style="width: 80%;">
        <div class="caption"><b>Electronics Maintenance Without Platform.</b> Accessing electronics on PEARL without a platform was a balancing act.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/maintenance_platform_test.jpg" alt="Maintenance Platform Prototype" style="width: 100%;">
        <div class="caption"><b>Platform Prototype.</b> I used the PEARL CAD assembly as a reference to design a geometry for a platform that could be slotted onto PEARL to more easily access the electronics case. This is a laser cut cardboard platform for design verification.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/maintenance_bending.jpg" alt="Platform Fabrication" style="width: 70%;">
        <div class="caption"><b>Platform Fabrication.</b> I waterjetted the platform and bent the flaps using a brake. I initially used .125" 2024 aluminum and it snapped in the brake. The second time around we opted for 0.090" 3003.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/maintenance_platform_complete.jpg" alt="Completed Maintenance Platform" style="width: 60%;">
        <div class="caption"><b>Completed Platform.</b> It fit perfectly! The flaps on the platform secured the platform against the 80/20.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-maintenance', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-maintenance', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

<div class="image-carousel-container">
    <h2 class="carousel-title">Community Outreach & Extras</h2>
    <div class="image-carousel" id="carousel-misc">
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/outreach1.jpeg" alt="Collecting Hydrophone Data" style="width: 80%;">
        <div class="caption"><b>Hydrophone Activity with Camp Students.</b> Camp students learned about PEARL’s hydrophone in a classroom. Then we went outside to get some fun recordings of the ocean. We also had some kids speak into the hydrophone.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/outreach2.jpg" alt="Visualizing Hydrophone Data" style="width: 100%;">
        <div class="caption"><b>Visualizing Hydrophone Audio.</b> Demonstrated how hydrophone data can be visualized, showing students the link between sounds and the graphs they generate.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/outreach3.jpg" alt="Collecting Hydrophone Data" style="width: 70%;">
        <div class="caption"><b>Collecting Hydrophone Data.</b> Students took turns to take hydrophone recordings from different locations. </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/pearl_content/outreach4.jpg" alt="Teaching about Hydrophone" style="width: 60%;">
        <div class="caption"><b>Hydrophone Lesson.</b> Every week we had a different lesson and activity planned for the students. Other topics included solar panels, water quality, and environmental monitoring. </div>
    </div>
    <div class="carousel-slide">
        <img src="/assets/images/pearl_content/biofouling.jpeg" alt="Biofouling" style="width: 60%;">
        <div class="caption"><b>Biofouling.</b> Biofouling on PEARL after only a couple weeks being in the water!</div>
      </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-misc', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-misc', 1)">&#10095;</button>
  </div>


</div>


<script>
  const currentIndices = {}; // Keeps track of index per carousel

  function scrollCarousel(id, direction) {
    const carousel = document.getElementById(id);
    const slides = carousel.querySelectorAll(".carousel-slide");

    // Initialize index if it's the first time
    if (!(id in currentIndices)) currentIndices[id] = 0;

    currentIndices[id] += direction;

    // Clamp the index
    if (currentIndices[id] < 0) currentIndices[id] = 0;
    if (currentIndices[id] >= slides.length) currentIndices[id] = slides.length - 1;

    const scrollAmount = slides[0].offsetWidth;

    // Scroll to the correct slide
    carousel.scrollTo({
      left: scrollAmount * currentIndices[id],
      behavior: 'smooth'
    });
  }
</script>


