
<div class="project-detail">
  <h1 class="project-title">{{ page.title }}</h1>
  <p class="project-dates">{{ page.date_range }}</p>

  <div class="project-section">
    <p>For my masters thesis I worked in the <a href="https://biomimetics.mit.edu/" target="_blank" rel="noopener">Biomimetic Robotics Lab</a> (BRL) under Prof. Sangbae Kim. I built off of prior work on barometer-based tactile sensors developed by students in BRL which demonstrated that neural networks could be used to infer contact location and force from barometric pressure sensors embedded within an elastomer. My work aimed to improve the robustness of this method and the practical deployment of these sensors to a robotic manipulation system.
    </p>
    <p>
    To this end, I:</p>
    <ul>
      <li>Created an automated data collection pipeline for capturing data at a fixed frequency, uniformly sampling across sensor surfaces, and including both in and out-of-contact samples.</li> 
      <li>Improved sensitivity and robustness of contact estimation by leveraging recurrent neural networks to model the elastomer’s viscoelastic response.</li>
      <li>Deployed the models on the sensor’s integrated microcontroller, enabling light grasping and contact-based rolling estimation using a multi-dof robotic gripper.</li>
    </ul>
    <p>
      This work was generalized across two sensor shapes - a sphere and ellipsoid. Adapting the work to the ellipsoid shape was notably more involved due to its lack of radial symmetry. You can read more about this work in my thesis.
    </p>
  </div>

<div class="project-section wide">
  <div class="gif-pair">
    <div class="gif-container">
      <img src="/assets/images/brl_content/sphere_web1x.gif" alt="Sphere Sensor Estimation">
      <p class="gif-caption">Spherical Sensor Contact Estimation</p>
    </div>
    <div class="gif-container">
      <img src="/assets/images/brl_content/ellipsoid_web1x.gif" alt="Ellipsoid Sensor Estimation">
      <p class="gif-caption">Ellipsoid Sensor Contact Estimation</p>
    </div>
  </div>
</div>




  <div class="image-carousel-container">
    <h2 class="carousel-title">Sensor Design</h2>
    <div class="image-carousel" id="carousel-intro">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/sensors_smaller.png" alt="Sensor Design">
        <div class="caption">Both tactile sensors used in this work feature eight barometers in a non-planar arrangement embedded within a curved cast elastomer. The cast ellipsoid on the ellipsoid sensor (top row) has semi-axes measurements of a=10.7mm, b=9mm, c=6.8mm. The cast sphere on the spherical sensor (bottom row) has a radius of 10mm. <p>Note: These sensors were designed prior to my work.</p></div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/sensorfab.png" alt="Sensor Fabrication">
        <div class="caption">Sensor fabrication process. The two-part Vytaflex 20 polyurethane is mixed and degassed using a vacuum chamber connected to a pump. This material is poured into a mold and left to cure. </div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/sensorPCB.png" alt="Sensor PCB">
        <div class="caption">The PCB consists of eight barometric pressure sensors shown in red (BMP384), a microcontroller (STM32F334), and five time-of-flight sensors shown in yellow (VL6180X). The right image shows a close-up of the barometer, with the circular feature indicating the cavity where the elastomer pours in.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-intro', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-intro', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

  <div class="image-carousel-container">
    <h2 class="carousel-title">Viscoelastic Effects</h2>
    <div class="image-carousel" id="carousel-visco">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/stressrecovery.png" alt="Stress Recovery" style="width: 80%;">
        <div class="caption">Normalized barometer readings plotted over repeated contacts for both tactile sensors. We find that the elastomer volume on the sensors introduces pronounced viscoelastic effects, such as stress relaxation and residual stress accumulation, which degrade model accuracy.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/barometerorientation.png" alt="Barometer Orientation Effects" style="width: 80%;">
        <div class="caption">The non-planar arrangement of barometers means that barometers are often at large angles to incoming contact forces. Data from two different barometers in the spherical sensor is shown over repeated contacts in the direction given by n_contact. As the angle between a barometer’s sensing axis and the contact normal increases, the modes of mechanical interaction between the elastomer and the barometer become more variable</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-visco', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-visco', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">


  <div class="image-carousel-container">
    <h2 class="carousel-title">Data Collection</h2>
    <div class="image-carousel" id="carousel-data">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/gantryhardware_diagram.png" alt="Gantry Hardware Diagram" style="width: 80%;">
        <div class="caption">Ground truth sensor data for both sensor geometries is collected with a custom five-axis gantry. The tactile sensor is mounted to the 3-axis linear stage. An ATI force sensor is mounted to the lower rotary stage.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/gantrysystem_diagram.png" alt="Gantry System Diagram" style="width: 80%;">
        <div class="caption">System diagram for data collection setup. All data is logged at 100Hz. Multithreading is used to sample position data from the actuators and sensor data from the Nucleo board while applying position control.</div>
      </div>
        <div class="carousel-slide">
        <img src="/assets/images/brl_content/gantry_run_ordered.gif" alt="Gantry Running" style="width: 80%;">
        <div class="caption">Example trajectory to sample points on the ellipsoid sensor, calculated using the inverse kinematics of the 5-axis gantry.</div>
      </div>
        <div class="carousel-slide">
        <img src="/assets/images/brl_content/uniform_and_sphere_coords.png" alt="Uniform vs. Spherical" style="width: 80%;">
        <div class="caption">Highlights difference between using discretized spherical coordinates for point generation, resulting in dense sampling near the poles, and the proposed uniform sampling method, which generates points uniformly over the surface. Uniform sampling ensures balanced coverage and reduces bias toward specific regions, promoting better generalization when learning models.
</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-data', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-data', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

  <div class="image-carousel-container">
    <h2 class="carousel-title">Neural Network Methods</h2>
    <div class="image-carousel" id="carousel-nn">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/neuralnets_binnedrnn.png" alt="Binned RNN" style="width: 100%;">
        <div class="caption">Proposed "Binned RNN": a two-layer recurrent neural network with binned angle outputs. "Binned" comes from the fact that the contact angle output ranges are discretized into bins and the network outputs a distribution indicating the likelihood that the contact angle falls within each bin. The final estimates of the contact angles are calculated as the sum of the bin centers, weighted by the network predictions. The input of the architecture is the eight barometer readings from the sensor. The final outputs are the 3-axis force in the sensor frame, the normal force, the contact location as Euler angles, and a contact flag.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/neuralnets.png" alt="Neural Network Comparison" style="width: 100%;">
        <div class="caption">To demonstrate improved contact estimation of the Binned RNN architecture, we perform ablations. The four neural network architectures tested are arranged in a 2×2 grid: columns group models by type (MLP vs. RNN), while rows group them by angle binning method. Binned versions include additional softmaxed output probability vectors, $\vec{p}$ and $\vec{q}$, which represent discretized distributions of probabilities over $\theta$ and $\phi$. These are converted to final angle estimates using a weighted average.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-nn', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-nn', 1)">&#10095;</button>
  </div>

  <hr class="carousel-separator">

  <div class="image-carousel-container">
    <h2 class="carousel-title">Neural Network Results</h2>
    <div class="image-carousel" id="carousel-nnresults">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/validation_plot.png" alt="Gantry Hardware Diagram" style="width: 75%;">
        <div class="caption">MLP and Binned RNN models are compared on data collected several weeks after initial data collection. The Binned RNN produces more accurate force and angle readings on the spherical sensor than the MLP. It also reduces angle drift during contact and decouples force and angle predictions. For the ellipsoid sensor, performance between models is more similar, which is to be expected given the lower elastomer volume.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/all_histograms_portrait.png" alt="Resolution Histograms" style="width: 80%;">
        <div class="caption">Sensor angular prediction error distributions across models for both contact angles. One standard deviation lines are shown on each plot. The binned architectures have consistently lower standard deviations of errors than non-binned.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/contact_flag_robustness.png" alt="Contact Flag" style="width: 80%;">
        <div class="caption">Ground truth force data over repeated contacts for the spherical sensor. Shaded regions mark where the predicted contact flag or thresholded predicted normal force detects contact. Explicit prediction of contact is more robust than thresholding predicted forces.</div>
      </div>
        <div class="carousel-slide">
        <img src="/assets/images/brl_content/results_table.png" alt="Results Table" style="width: 80%;">
        <div class="caption">Ablation results. All binned architectures yield lower angular RMSEs than their non-binned counterparts. RNN models have a lower RMSE and BCE loss on all prediction targets except for phi_ellipsoid.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-nnresults', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-nnresults', 1)">&#10095;</button>
  </div>
  
  <hr class="carousel-separator">

  <div class="image-carousel-container">
    <h2 class="carousel-title">Experimental Validation</h2>
    <div class="image-carousel" id="carousel-validation">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/mujoco_ellipsoid.gif" alt="MuJoCo Interface" style="width: 80%;">
        <div class="caption">Contact estimate of Binned RNN displayed in MuJoCo environment for ellipsoid sensor in real time.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/propriovtactile_web.gif" alt="Proprioception vs Tactile" style="width: 110%;">
        <div class="caption">Cylinder rotation is approximated first using proprioception only and then with added tactile estimates using the Binned RNN. Proprioception provides a rough estimate of cylinder orientation, but the addition of tactile input closes the gap between the estimated and the ground truth positions.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/sphere_rolling_web.gif" alt="Sphere Rolling Experiment" style="width: 110%;">
        <div class="caption">Cylinder rotation is estimated using a combination of proprioception and tactile sensing. Contact estimates from the Binned RNN versus Non-Binned MLP are used to calculate the orientation of the cylinder. The gripper is command to restart the algorithm when an angle of 90 degrees has been reached.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/ellipsoid_rolling_web.gif" alt="Ellipsoid Rolling Experiment" style="width: 110%;">
        <div class="caption">Cylinder rotation is estimated using a combination of proprioception and tactile sensing. Contact estimates from the Binned RNN versus Non-Binned MLP are used to calculate the orientation of the cylinder. The gripper is command to restart the algorithm when an angle of 90 degrees has been reached.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-validation', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-validation', 1)">&#10095;</button>
  </div>

  
  <!-- <hr class="carousel-separator"> -->

  <!-- <div class="image-carousel-container">
    <h2 class="carousel-title">Extras</h2>
    <div class="image-carousel" id="carousel-extras">
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/validation_plot.png" alt="PCB Design" style="width: 75%;">
        <div class="caption">MLP and Binned RNN models are compared on data collected several weeks after initial data collection. The Binned RNN produces more accurate force and angle readings on the spherical sensor than the MLP. It also reduces angle drift during contact and decouples force and angle predictions. For the ellipsoid sensor, performance between models is more similar, which is to be expected given the lower elastomer volume.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/all_histograms_portrait.png" alt="Resolution Histograms" style="width: 80%;">
        <div class="caption">Sensor angular prediction error distributions across models for both contact angles. One standard deviation lines are shown on each plot. The binned architectures have consistently lower standard deviations of errors than non-binned.</div>
      </div>
      <div class="carousel-slide">
        <img src="/assets/images/brl_content/contact_flag_robustness.png" alt="Contact Flag" style="width: 80%;">
        <div class="caption">Ground truth force data over repeated contacts for the spherical sensor. Shaded regions mark where the predicted contact flag or thresholded predicted normal force detects contact. Explicit prediction of contact is more robust than thresholding predicted forces.</div>
      </div>
        <div class="carousel-slide">
        <img src="/assets/images/brl_content/results_table.png" alt="Results Table" style="width: 80%;">
        <div class="caption">Ablation results. All binned architectures yield lower angular RMSEs than their non-binned counterparts. RNN models have a lower RMSE and BCE loss on all prediction targets except for phi_ellipsoid.</div>
      </div>
    </div>
    <button class="arrow left" onclick="scrollCarousel('carousel-extras', -1)">&#10094;</button>
    <button class="arrow right" onclick="scrollCarousel('carousel-extras', 1)">&#10095;</button>
  </div> -->

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
