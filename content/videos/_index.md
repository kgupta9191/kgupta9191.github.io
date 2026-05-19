---
title: Videos
type: landing
cms_exclude: true

sections:
  - block: markdown
    content:
      title: Computational Flow Visualizations
      subtitle: Selected simulation videos, research animations, and machine-learning demonstrations.
      text: |-
        <style>
          .video-section {
            margin-bottom: 3rem;
          }

          .video-grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            align-items: start;
            margin-bottom: 1.25rem;
          }

          .video-grid-2 {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            align-items: start;
            margin-bottom: 1.25rem;
          }

          .video-grid-1 {
            display: grid;
            grid-template-columns: repeat(1, 1fr);
            gap: 1rem;
            align-items: start;
            margin-bottom: 1.25rem;
          }

          .video-card {
            width: 100%;
          }

          .video-card h3 {
            margin-top: 0;
            margin-bottom: 0.4rem;
            font-size: 1rem;
            text-align: center;
          }

          .video-card video {
            width: 100%;
            height: auto;
            max-height: 320px;
            object-fit: contain;
            border-radius: 12px;
            display: block;
            background: #000;
          }

          .video-description {
            margin-top: 1rem;
            font-size: 1rem;
            line-height: 1.7;
          }

          @media (max-width: 900px) {
            .video-grid-3 {
              grid-template-columns: repeat(2, 1fr);
            }
          }

          @media (max-width: 600px) {
            .video-grid-3,
            .video-grid-2 {
              grid-template-columns: 1fr;
            }

            .video-card video {
              height: 240px;
            }
          }
        </style>

        <div class="video-section">

        ## Vertical Water Entry

        <div class="video-grid-3">

          <div class="video-card">
            <h3>Concave Nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/vertical_entry/dr-2_0deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>Flat Nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/vertical_entry/dr0_0deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>Convex Nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/vertical_entry/dr2_0deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

        </div>

        <div class="video-description">
        These Blender-rendered visualizations show the effect of nose curvature (concave, flat, and convex noses) during vertical water entry. They highlight how nose shape influences splash formation, air cavity evolution, and cavity closure dynamics (Froude No. = 4).
        </div>

        </div>

        ---

        <div class="video-section">

        ## Tilted Water Entry

        <div class="video-grid-3">

          <div class="video-card">
            <h3>θ = 0°</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/vertical_entry/dr0_0deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>θ = 3°</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/tilted_entry/dr0_3deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>θ = 5°</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/tilted_entry/dr0_5deg.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

        </div>

        <div class="video-description">
        These visualizations compare tilted water-entry cases with the no-tilt case. They highlight how the tilt angle influences splash formation, air cavity evolution, and cavity closure dynamics (Fr = 4, Concave nose).
        </div>

        </div>

        ---

        <div class="video-section">

        ## Spinning Water Entry

        <div class="video-grid-3">

          <div class="video-card">
            <h3>St = 0</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/spinning_entry/dr-2_5deg_st0.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>St = 1</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/spinning_entry/dr-2_5deg_st1.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>St = 2</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/spinning_entry/dr-2_5deg_st2.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

        </div>

        <div class="video-description">
        These Blender visualizations compare spinning water-entry cases with the no-spin case. They highlight how the spin parameter, St = rω/U₀, influences splash formation, air cavity evolution, and cavity closure dynamics (Fr = 4, θ = 5°, Concave nose).
        </div>

        </div> 

        ---

        <div class="video-section">

        ## Oscillating Plate

        <div class="video-grid-1">

          <div class="video-card">
            <h3></h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/oscillating_plate/vorticity.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

        </div>

        <div class="video-description">
        This VisIt-rendered visualization shows the vorticity field generated by an oscillating plate near the air–water interface. The video highlights how the plate motion influences free-surface deformation, vortex formation, and the near-interface flow evolution.
        </div>

        </div>       

        ---

        <div class="video-section">

        ## Added Mass Evolution

        <div class="video-grid-3">

          <div class="video-card">
            <h3>Concave nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/added_mass/dr-2_cropped.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>Flat nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/added_mass/dr0_cropped.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

          <div class="video-card">
            <h3>Convex nose</h3>
            <video autoplay muted loop playsinline controls>
              <source src="/videos/added_mass/dr2_cropped.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>

        </div>

        <div class="video-description">
         The video shows the added mass evolution of a solid cylinder of different nose curvatures impacting the water free-surface at θ = 5° (tilted entry).
        </div>

        </div>

        ---

        ##### > **Copyright Notice:** All videos and Blender visualizations on this page are created by Kartik Gupta and are protected by copyright. Please contact the author for permission before using, reproducing, redistributing, or modifying any of these materials.

    design:
      columns: '1'
---
