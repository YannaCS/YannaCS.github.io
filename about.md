---
layout: about
title: About Me
menu: true
order: 1
---
<!-- to change header's intro, go to /_data/authors.yml -->
<style>
/* Timeline Styles */
.timeline-container {
  max-width: 1600px;
  margin: 60px auto;
  position: relative;
  padding: 20px 30px; /*top and bottom, left and right*/
}

/* Central line */
.timeline-container::before {
  content: '';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 4px;
  height: calc(100% + 20px); /* Extend the line to reach the Future node */
  background: linear-gradient(to bottom, #4fb1ba, #4f8ef7);
  top: -20px;
}

/* Timeline item */
.timeline-item {
  position: relative;
  width: 100%;
  margin-bottom: -50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: all 0.3s ease;
  min-height: 200px;
}

/* Alternating sides */
.timeline-item:nth-child(odd) {
  flex-direction: row-reverse;
}

/* Content box */
.timeline-content {
  width: 550px;
  max-width: 47%;
  position: relative;
  cursor: pointer;
  perspective: 1000px;
  overflow: hidden; /* Prevent content overflow */
}

/* Flip container */
.timeline-flip-container {
  position: relative;
  width: 100%;
  transform-style: preserve-3d;
  transition: transform 0.6s;
  min-height: inherit; /* Inherit from parent */
}

/* Flip state */
.timeline-content.flipped {
  overflow: hidden;
  border-radius: 10px; /* Maintain border radius */
}
.timeline-content.flipped .timeline-flip-container {
  transform: rotateY(180deg);
}


/* Front and back faces */
.timeline-front,
.timeline-back {
  width: 100%;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  background: #f8f9fa;
  padding: 10px 25px;  /*top and bottom, right and left*/
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
  box-sizing: border-box;
}

/* Front face */
.timeline-front {
  position: relative;
}

/* Back face */
.timeline-back {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  transform: rotateY(180deg);
  min-height: 100%;
  max-height: 100%; /* Limit to parent height */
  overflow-y: auto; /* Add scrolling for long content */
  overflow-x: hidden; /* Prevent horizontal scroll */
  word-wrap: break-word;
  word-break: break-word;
  z-index: 2; /* Add this to place content above the timeline line */
  background: #f8f9fa; /* Ensure solid background */
}
/* Optional: Style the scrollbar */
.timeline-back::-webkit-scrollbar {
  width: 6px;
}

.timeline-back::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 3px;
}

.timeline-back::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 3px;
}

.timeline-back::-webkit-scrollbar-thumb:hover {
  background: #555;
}
/* scrollbar end*/

/* Adjust h3 title spacing */
.timeline-back h3 {
  margin-top: 0;
  padding-right: 40px; /* Make room for close button */
  font-size: 1em;
}

/* Hover effects */
.timeline-content:hover .timeline-flip-container {
  transform: translateY(-5px);
}

.timeline-content.flipped:hover .timeline-flip-container {
  transform: rotateY(180deg) translateY(-5px);
}

/* Add border highlight */
.timeline-content::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border: 2px solid transparent;
  border-radius: 10px;
  transition: all 0.3s ease;
  pointer-events: none;
  z-index: 1;
}

.timeline-content:hover::before {
  border-color: #4fb1ba;
}

/* Bullet list inside timeline */
.timeline-bullets {
  margin: 10px 0;
  padding-left: 0;
  list-style: none;
}

.timeline-bullets li {
  position: relative;
  padding-left: 20px;
  margin-bottom: 6px;
  font-size: 0.9em;
  /*color: #555;*/
  line-height: 1.4;
}

.timeline-bullets li::before {
  content: "•";
  position: absolute;
  left: 0;
  /*color: #4fb1ba;*/
  font-weight: bold;
  font-size: 0.9em; /*1.2*/
}

/* Subtle animation for bullets on hover */
.timeline-content:hover .timeline-bullets li {
  transform: translateX(5px);
  transition: transform 0.3s ease;
}

/* Click indicator */
.timeline-click-hint {
  position: absolute;
  bottom: 10px;
  right: 15px;
  font-size: 0.8em;
  color: #999;
  display: flex;
  align-items: center;
  gap: 5px;
}

.timeline-click-hint::before {
  content: "🔄";
  font-size: 1em;
}

/* Back button */
.timeline-back-btn {
  position: absolute;
  top: 15px;  /*20px*/
  right: 10px;  /*35px*/
  background: #4fb1ba;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 0.8em;
  z-index: 10;
}

.timeline-back-btn:hover {
  background: #3a8a92;
}

/* Details section styling */
.timeline-details {
  margin-top: 1px;
  padding-bottom: 20px; /* Add bottom padding */
  font-size: 0.9em;
}

.timeline-details h4 {
  color: #2c3e50;
  margin-bottom: 2px;
  margin-top: 2px; /* Add specific top margin */
  font-size: 0.9em;
  word-wrap: break-word;
  word-break: break-word;
}
/* First h4 should have less space */
.timeline-details h4:first-child {
  margin-top: 1px; /* Much less space for the first h4 */
}
/* Ensure lists don't overflow */
.timeline-details ul {
  list-style: none;
  padding: 0;
  margin: 0 0 15px 0; /* Add bottom margin between sections */
}

.timeline-details li {
  padding-left: 20px;
  padding-right: 10px; /* Add right padding */
  position: relative;
  margin-bottom: 8px;
  color: #555;
  font-size: 0.9em;
  word-wrap: break-word; /* Force word breaking */
  word-break: break-word; /* Better browser support */
  hyphens: auto; /* Allow hyphenation */
  line-height: 1.5; /* Better line spacing */
}

.timeline-details li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4fb1ba;
}
/* Regular text (like "plz view...") */
.timeline-details p,
.timeline-details div {
  font-size: 0.8em; /* Add this for non-list text */
  line-height: 1.4;
}

/* Arrow pointing to timeline */
.timeline-item:nth-child(even) .timeline-front::after,
.timeline-item:nth-child(even) .timeline-back::after {
  content: '';
  position: absolute;
  right: -15px;
  top: 50%;
  transform: translateY(-50%);
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 15px 0 15px 15px;
  border-color: transparent transparent transparent #f8f9fa;
}

.timeline-item:nth-child(odd) .timeline-front::after,
.timeline-item:nth-child(odd) .timeline-back::after {
  content: '';
  position: absolute;
  left: -15px;
  top: 50%;
  transform: translateY(-50%);
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 15px 15px 15px 0;
  border-color: transparent #f8f9fa transparent transparent;
}

/* Make the entire timeline item interactive */
.timeline-item:hover .timeline-content .timeline-meta .company a {
  color: #2d7a84;
}

/* Timeline node */
.timeline-node {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 40px;
  height: 40px;
  background: white;
  border: 4px solid #4fb1ba;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
  transition: all 0.3s ease;
}

.timeline-node:hover {
  transform: translateX(-50%) scale(1.2);
  border-color: #4f8ef7;
}

/* Enhance node on content hover */
.timeline-item:hover .timeline-node {
  transform: translateX(-50%) scale(1.2);
  box-shadow: 0 0 20px rgba(79, 177, 186, 0.4);
}

/* Different colors for each node */
/*
.timeline-item:nth-child(1) .timeline-node { border-color: #4fb1ba; }
.timeline-item:nth-child(2) .timeline-node { border-color: #f39c12; }
.timeline-item:nth-child(3) .timeline-node { border-color: #e74c3c; }
.timeline-item:nth-child(4) .timeline-node { border-color: #9b59b6; }
.timeline-item:nth-child(5) .timeline-node { border-color: #3498db; }
.timeline-item:nth-child(6) .timeline-node { border-color: #2ecc71; }
*/
/* Dynamic color matching based on year color */
.timeline-item .timeline-node {
  /* Border color will be set dynamically */
}

/* Year label */
.timeline-year {
  font-size: 0.9em;
  font-weight: bold;
  color: #333;
  margin-bottom: 8px;
  /*margin: 0px 0px 2px 0px; /* top right bottom left */
}

/* Milestone title */
.timeline-title {
  font-size: 1em;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 8px;
  text-transform: uppercase;
  white-space: normal;
  line-height: 1.3;
}

/* Brighten colors on hover */
.timeline-item:hover .timeline-year {
  filter: brightness(1.1);
}

.timeline-item:hover .timeline-title {
  color: #4fb1ba;
}

/* Company and Location in one line*/
/* Meta line with company and location */
.timeline-meta {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 8px;
  font-size: 0.9em;
}

.timeline-meta .company {
  font-weight: 600;
}

.timeline-meta .company a {
  color: #4fb1ba;
  text-decoration: none;
  transition: all 0.2s ease;
}

.timeline-meta .company a:hover {
  color: #3a8a92;
  text-decoration: underline;
}

.timeline-meta .separator {
  color: #bdc3c7;
  font-size: 0.85em;
}

.timeline-meta .location {
  color: #7f8c8d;
  display: flex;
  align-items: center;
  gap: 4px;
}

.timeline-meta .location::before {
  content: "📍";
  font-size: 0.85em;
}
/* Company and Location - END*/

/* Description */
.timeline-description {
  color: #555;
  line-height: 1.6;
  font-size: 0.9em;
}

/* Icons */
.timeline-icon {
  font-size: 20px;
  color: white;
}
/* Make icons white for better contrast on colored backgrounds */
.timeline-node .timeline-icon {
  color: white;
  filter: drop-shadow(0 1px 2px rgba(0,0,0,0.2));
}

/* Start and Finish markers */
.timeline-marker {
  background: #2c3e50;
  color: white;
  padding: 10px 25px;
  border-radius: 25px;
  font-weight: bold;
  text-align: center;
  margin: 30px auto;
  width: fit-content;
}
/* Make sure the PRESENT marker has proper spacing */
.timeline-marker:first-of-type {
  margin-top: 10px;
  margin-bottom: 50px;
}

/* No flip class - removes cursor and prevents flip */
.timeline-content.no-flip {
  cursor: default;
}

/* Remove hover effects for no-flip items */
.timeline-content.no-flip:hover .timeline-flip-container {
  transform: none;
}

.timeline-content.no-flip:hover::before {
  border-color: transparent;
}

/* Optional: Add a visual indicator that it's not clickable */
.timeline-content.no-flip .timeline-description {
  padding-bottom: 15px; /* Add some bottom padding since no click hint */
}

/* Special styling for Future item */
.timeline-item:first-child {
  margin-top: -30px; /* Pull the item up */
}
.timeline-item:first-child .timeline-node {
  border-color: #92B8BE;
  background: #92B8BE;
  color: white;
  top: -20px; /* Position node at the start of the line */
}

.timeline-item:first-child .timeline-content {
  background: linear-gradient(135deg, #f8f9fa 0%, #e8f5e9 100%);
}

/* Optional: Add a subtle animation to the future node */
@keyframes pulse {
  0% {
    box-shadow: 0 0 0 0 rgba(46, 204, 113, 0.7);
  }
  70% {
    box-shadow: 0 0 0 10px rgba(46, 204, 113, 0);
  }
  100% {
    box-shadow: 0 0 0 0 rgba(46, 204, 113, 0);
  }
}

.timeline-item:first-child .timeline-node {
  animation: pulse 2s infinite;
}
/* For the Future item specifically (green) */
.timeline-year[style*="color: #92B8BE"] ~ * ~ * .timeline-node,
.timeline-year[style*="color: #92B8BE"] ~ * ~ * ~ .timeline-node {
  border-color: #92B8BE !important;
}
/* Skill Grid */
.skill-grid {
  margin-top: 0px !important; /* Reduce from 40px */
}
.skill-category {
  padding: 15px 20px; /* Add padding inside each card */
  border-radius: 8px;
  margin-top: 10px;
  transition: all 0.3s ease;
  background: #f8f9fa; /* Light background */
}

.skill-category:hover {
  transform: translateY(-3px);
  background: rgba(0,0,0,0.02);
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}
/* Reduce heading size and margin */
.skill-category h3 {
  font-size: 1em; /* Smaller heading */
  margin-bottom: 10px; /* Less space after heading */
  margin-top: 0;
}

/* Make list more compact */
.skill-category ul {
  margin: 0;
  padding-left: 20px; /* Less indent */
  list-style-type: disc; /* Add bullets */
}

.skill-category li {
  margin-bottom: 4px; /* Less space between items */
  font-size: 0.9em; /* Slightly smaller text */
}

/* Style for emphasis - Make the "HIRE ME!" more prominent */
/*strong:contains("HIRE ME") {
  color: #e74c3c;
  font-size: 1.1em;
}*/
.hire-me {
  color: #e74c3c;
  font-size: 1.2em;
  font-weight: bold;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
  animation: sparkle 2s infinite;
}

@keyframes sparkle {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}

/* Dog section styling */
.dog-section {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  margin: 20px 0;
}
.dog-text {
  flex: 1;
}
.dog-image {
  flex: 0 0 300px;
}
.dog-image img {
  width: 100%;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}


/* Responsive design */
/* Large screens */
@media (max-width: 1400px) and (min-width: 969px) {
  .timeline-content {
    width: 450px;
    max-width: 46%;
  }
  
  .timeline-container {
    padding: 0 0px;
  }
}

/* Tablet/half-screen */
@media (max-width: 968px) and (min-width: 600px) {
  .timeline-content {
    width: 400px;
    max-width: 46%;
  }
  
  .timeline-container {
    padding: 0 0px;
  }
  
  /* Reduce font sizes slightly */
  .timeline-title {
    font-size: 1em;
  }
  
  .timeline-description {
    font-size: 0.85em;
  }
  
  .timeline-details li {
    font-size: 0.85em;
  }
  
  /* Adjust padding */
  .timeline-front,
  .timeline-back {
    padding: 5px 10px;
  }
}

/* Mobile view */
@media (max-width: 599px) {
  .timeline-container {
    padding: 0 0px;
  }
  
  /*line and node with icon*/
  .timeline-container::before {
    left: 6px; 
  }
  .timeline-node {
    left: 6px;  /*30*/
  }

  .timeline-item {
    flex-direction: column !important;
    align-items: flex-start !important;
    min-height: auto;
    margin-bottom: 30px;
  }
  
  .timeline-content {
    width: calc(100% - 20px);
    max-width: 98%;
    margin-left: 30px;
  }
  
  /* Adjust padding */
  .timeline-front,
  .timeline-back {
    padding: 5px 10px;
  }
  
  .timeline-front::after,
  .timeline-back::after {
    display: none;
  }
}

/* for words around dog plot */
@media (max-width: 768px) {
  .dog-section {
    flex-direction: column;
    gap: 15px;
  }
  
  .dog-text {
    flex: none;
    width: 100%;
  }
  
  .dog-image {
    flex: none;
    width: 100%;
    max-width: 400px;
    margin: 0 auto;
  }
}

/* Very small screens */
@media (max-width: 480px) {
  .dog-image {
    max-width: 100%;
  }
}

</style>
<div class="hint">
  <span class="hint-icon">💡</span>
  <span class="hint-text">Click cards for details</span>
</div>

<!-- Content -->
<h2>Here's where I am presently, and where I'm headed</h2>

<!-- Time line items -->
<!-- <div class="timeline-marker">PRESENT</div> -->
<div class="timeline-container">

  <!-- Future -->
  <div class="timeline-item">
  <div class="timeline-content no-flip">
    <div class="timeline-flip-container">
      <div class="timeline-front">
        <div class="timeline-year" style="color: #92B8BE;">Future</div>
        <div class="timeline-title">Tech Related Roles</div>
        <div class="timeline-meta">
          <span class="company">Open to Sponsorship</span>
          <span class="location">Open to Relocation</span>
        </div>
        <div class="timeline-description">
          <ul class="timeline-bullets">
            <li>3-Years OPT (STEM qualified), NO need of sponsorship</li>
            <li>After 3 years: I can bring you <b>more profits</b> than a lot people who don't need sponsorship</li>
            <li>Do you wanna contribute to my future life? <b>Hire Me!</b></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <div class="timeline-node" style="border-color: #92B8BE; background-color: #92B8BE;">
    <span class="timeline-icon">📈</span>
  </div>
</div>

  <!-- NEU -->
  <div class="timeline-item">
    <div class="timeline-content" onclick="flipCard(this)">
      <div class="timeline-flip-container">
        <!-- Front Face -->
        <div class="timeline-front">
          <div class="timeline-year" style="color: #DD848C;">May 2025</div>
          <div class="timeline-title">Master of Science in Data Analytics</div>
          <div class="timeline-meta">
            <span class="company"><a href="https://www.northeastern.edu/" target="_blank" onclick="event.stopPropagation();">Northeastern University</a></span>
            <span class="location">Seattle, WA</span>
          </div>
          <div class="timeline-description">
            <ul class="timeline-bullets">
              <li>Graduated with GPA 3.96/4.0</li>
              <li>Focus on: Data Science, Data Engineering, ML/AI, Cloud Computing, Database, Algorithms</li>
              <li>Certified: Tableau Data Analyst, AWS, Applied AI</li>
            </ul>
          </div>
        </div>
        
        <!-- Back Face -->
        <div class="timeline-back">
          <button class="timeline-back-btn" onclick="flipCard(this.closest('.timeline-content')); event.stopPropagation();">✕</button>
          <div class="timeline-details">
            <h4>Time Range</h4>
              Sept. 2023 - May 2025
            <h4>Projects</h4>
              Please view <a href="https://yannacs.github.io/projects/" target="_blank" onclick="event.stopPropagation();">Projects Page</a>
            <h4>Relevant Coursework</h4>
              <ul>
                <li>Data Analytics Engineering</li>
                <li>Deterministic Operations Research</li>
                <li>Data Mining</li>
                <li>Data Management and Database Design</li>
                <li>Visualization for Analytics</li>
                <li>Cloud Computing</li>
                <li>Data Structure</li>
                <li>Algorithms</li>
                <li>Statistic</li>
              </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="timeline-node" style="border-color: #DD848C; background-color: #DDB4AB;">
      <span class="timeline-icon">👩🏻‍🎓</span>
    </div>
  </div>

  <!-- Uplift Northwest -->
  <div class="timeline-item">
    <div class="timeline-content" onclick="flipCard(this)">
      <div class="timeline-flip-container">
        <!-- Front Face -->
        <div class="timeline-front">
          <div class="timeline-year" style="color: #81C59D;">June - Sept. 2024</div>
          <div class="timeline-title">Data Engineer Intern (Full Stack)</div>
          <div class="timeline-meta">
            <span class="company"><a href="https://www.linkedin.com/company/upliftnorthwest/posts/?feedView=all" target="_blank" onclick="event.stopPropagation();">Uplift Northwest</a></span>
            <span class="location">Seattle, WA</span>
          </div>
          <div class="timeline-description">
            <ul class="timeline-bullets">
              <li>Unified data systems via ETL pipelines and warehouse modeling.</li> 
              <li>Built Tableau dashboards and predictive models to drive business insights.</li>
            </ul>
          </div>
        </div>
        
        <!-- Back Face -->
        <div class="timeline-back">
          <button class="timeline-back-btn" onclick="flipCard(this.closest('.timeline-content')); event.stopPropagation();">✕</button>
          <div class="timeline-details">
            <h4>Key Achievements:</h4>
            <ul>
              <li>Streamlined data quality monitoring and reporting, cutting manual workload by 25% and improving reliability</li>
              <li>Audited and optimized database schemas by resolving normalization issues and improving data design</li>
              <li>Designed and deployed ETL pipelines to unify disparate data sources into a centralized warehouse</li>
              <li>Built interactive Tableau dashboards with drill-down views to visualize key performance indicators</li>
              <li>Developed ML models to predict client outcomes, using feature engineering and scikit-learn for performance gains</li>
              <li>Automated routine data validation processes, boosting consistency and operational efficiency</li>
            </ul>
            
            <h4>Technical Stack:</h4>
            <ul>
              <li>ETL: Apache Airflow, Python, SQL</li>
              <li>Visualization: Tableau</li>
              <li>ML: Scikit-learn, TensorFlow</li>
              <li>Database: MySQL, Salesforce, StarUML</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="timeline-node" style="border-color: #81C59D; background-color: #B4C5B8;">
      <span class="timeline-icon">🚀</span>
    </div>
  </div>

  <!-- Zhejiang Earthview -->
  <div class="timeline-item">
    <div class="timeline-content" onclick="flipCard(this)">
      <div class="timeline-flip-container">
        <!-- Front Face -->
        <div class="timeline-front">
          <div class="timeline-year" style="color: #60AED3;">Sept. 2020 - May 2022</div>
          <div class="timeline-title">Data Analyst</div>
          <div class="timeline-meta">
            <span class="company"><a href="https://www.ev-image.com/" target="_blank" onclick="event.stopPropagation();">Zhejiang Earthview Image Inc.</a></span>
            <span class="location">China</span>
          </div>
          <div class="timeline-description">
            <ul class="timeline-bullets">
              <li>Built ETL pipeline for satellite data (TB-scale) </li> 
              <li>Trained CV models (87% accuracy) for rural condition detection </li>
              <li>Contributed to ML project recognized in national competition</li>
            </ul>
          </div>
          <!-- <div class="timeline-click-hint">Click for details</div> -->
        </div>
        
        <!-- Back Face -->
        <div class="timeline-back">
          <button class="timeline-back-btn" onclick="flipCard(this.closest('.timeline-content')); event.stopPropagation();">✕</button>  
          <div class="timeline-details">
            <h4>Key Achievements:</h4>
            <ul>
              <li>Built computer vision models to detect rural environmental conditions, achieving 87% classification accuracy</li>
              <li>Designed and executed A/B tests to evaluate platform features and analyze user engagement</li>
              <li>Performed statistical analysis on usage data to uncover drivers of user retention and feature adoption</li>
              <li>Contributed to a nationally recognized ML project for environmental monitoring and policy insights</li>
            </ul>
            
            <h4>Technical Stack:</h4>
            <ul>
              <li>Data Analysis: Excel(VBA, PivotTable, Aggregate Function), Python(Pandas, Seaborn, Matplotlib), SQL, A/B Testing</li>
              <li>Computer Vision: OpenCV, TensorFlow, PyTorch</li>
              <li>Project Management: Microsoft(Teams, Project)</li>
              <li>Languages: Python, SQL, HTML</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="timeline-node" style="border-color: #60AED3; background-color: #ACCFD3;">
      <span class="timeline-icon">📊</span>
    </div>
  </div>

  <!-- XMU -->
  <div class="timeline-item">
    <div class="timeline-content" onclick="flipCard(this)">
      <div class="timeline-flip-container">
        <!-- Front Face -->
        <div class="timeline-front">
          <div class="timeline-year" style="color: #506076;">Aug. 2021</div>
          <div class="timeline-title">Bachelor of Engineering in Computer Science and Technology</div>
          <div class="timeline-meta">
            <span class="company"><a href="https://www.xmu.edu.my/" target="_blank" onclick="event.stopPropagation();">Xiamen University</a></span>
            <span class="location">Malaysia</span>
          </div>
          <div class="timeline-description">
            Graduated with <b>Honors</b>.
          </div>
          <!-- <div class="timeline-click-hint">Click for details</div> -->
        </div>
        
        <!-- Back Face -->
        <div class="timeline-back">
          <button class="timeline-back-btn" onclick="flipCard(this.closest('.timeline-content')); event.stopPropagation();">✕</button>
          <!-- <h3 style="color: #e74c3c; margin-bottom: 15px;">Academic Excellence</h3> -->
          
          <div class="timeline-details">
            <h4>Achievements:</h4>
            <ul>
              <li>Top 10% for all semesters</li>
              <li>President of Youth Leader Club</li>
              <li>3 Entrepreneurship Competition Top Awards</li>
              <li>Published research on fraud detection</li>
              <li>Maintained A's in all mathematics courses</li>
            </ul>
            
            <h4>Core Competencies:</h4>
            <ul>
              <li>Data Structures & Algorithms</li>
              <li>Database Management Systems</li>
              <li>Machine Learning & AI</li>
              <li>Software Engineering</li>
              <li>Computer Architecture & Networks</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="timeline-node" style="border-color: #506076; background-color: #7C96BB;">
      <span class="timeline-icon">🎓</span>
    </div>
  </div>

  <!-- Fraud Detection -->
  <div class="timeline-item">
    <div class="timeline-content" onclick="flipCard(this)">
      <div class="timeline-flip-container">
        <!-- Front Face -->
        <div class="timeline-front">
          <div class="timeline-year" style="color: #EEA53A;">Feb. - Aug. 2020</div>
          <div class="timeline-title">Data Science Researcher</div>
          <div class="timeline-meta">
            <span class="company">Prof. Stephen Coggeshall's Research Group</span>
            <span class="location">Online</span>
          </div>
          <div class="timeline-description">
            <ul class="timeline-bullets">
              <li>Built fraud detection model (99.07% accuracy, 1M+ txns) </li> 
              <li>Engineered features & validated via out-of-time testing </li>
              <li>Published in MLBDBI 2020 <a href="https://ieeexplore.ieee.org/abstract/document/9361052?casa_token=cM9hxNzoQsMAAAAA:MSSrhPp0tk7Q7OFTmakg4IA3tdDQeqa0Lde-4y62e-HHLzm8ouVv1-ZVdE5yzLmmuQa9Sm7RgzQ" target="_blank" onclick="event.stopPropagation();">(DOI: 10.1109/MLBDBI51377.2020.00025)</a></li>
            </ul>
          </div>
          <!-- <div class="timeline-click-hint">Click for details</div> -->
        </div>
        
        <!-- Back Face -->
        <div class="timeline-back">
          <button class="timeline-back-btn" onclick="flipCard(this.closest('.timeline-content')); event.stopPropagation();">✕</button>
          
          <div class="timeline-details">
            <h4>Key Achievements:</h4>
            <ul>
              <li>Cleaned and transformed 1M+ financial transactions, resolving missing values and outliers</li>
              <li>Engineered features using statistical methods (SelectKBest) and ROC-AUC–driven selection</li>
              <li>Applied out-of-time validation to simulate real-world fraud model deployment</li>
              <li>Optimized Different Decision Tree models (GBDT, LightGBM, XGBoost) with Bayesian hyperparameter tuning, reaching 99.07% accuracy</li>
              <li>Published research methodology and results in IEEE conference proceedings (DOI: 10.1109/MLBDBI51377.2020.00025)</li>
            </ul>
            
            <h4>Updated Project Details:</h4>
            Plz view <a href="https://yannacs.github.io/projects/fraud%20detection/" target="_blank" onclick="event.stopPropagation();">Projects Page</a>
          </div>
        </div>
      </div>
    </div>
    <div class="timeline-node" style="border-color: #EEA53A; background-color: #F6CE94;">
      <span class="timeline-icon">🤖</span>
    </div>
  </div>
  <!-- END ITEMS -->
</div>

<div class="timeline-marker">START</div>

<h2>Skills & Expertise</h2>
<div class="skill-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 10px; margin-top: 1px;">

  <div class="skill-category">
    <h3 style="color: #2ecc71;">Certifications & Certificates</h3>
    <ul>
      <li>Tableau Certified Data Analyst</li>
      <li>AI Literacy Certificate</li>
      <li>Graduate Leadership Certificate</li>
      <li>Data Analytics on AWS</li>
      <li>Applied AI Certificate</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #9b59b6;">Programming Languages</h3>
    <ul>
      <li>Python (Advanced)</li>
      <li>SQL (MySQL, NoSQL)</li>
      <li>Java & JSP</li>
      <li>C/C++</li>
      <li>MATLAB</li>
      <li>Shell Scripting</li>
      <li>MIPS Assembly</li>
      <li>HTML</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #34495e;">Software Engineering</h3>
    <ul>
      <li>Data Structures</li>
      <li>Algorithms</li>
      <li>Database Design</li>
      <li>API Integration</li>
      <li>Web Development</li>
      <li>Security Best Practices</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #4fb1ba;">Data Engineering</h3>
    <ul>
      <li>ETL Pipeline Development</li>
      <li>Database Design & Normalization</li>
      <li>Data Warehousing</li>
      <li>Data Cleaning & Processing</li>
      <li>Data Ingestion & Storage</li>
      <li>Apache Spark & Kafka</li>
      <li>BigQuery</li>
    </ul>
  </div>
  
  <div class="skill-category">
    <h3 style="color: #f39c12;">Machine Learning & AI</h3>
    <ul>
      <li>TensorFlow</li>
      <li>Scikit-learn</li>
      <li>NLP & Computer Vision</li>
      <li>Predictive Modeling</li>
      <li>Feature Engineering</li>
      <li>Time Series Analysis</li>
      <li>Clustering (K-Means, KNN)</li>
      <li>PCA & t-SNE</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #e67e22;">Analytics & Statistics</h3>
    <ul>
      <li>Statistical Analysis</li>
      <li>A/B Testing</li>
      <li>Sentiment Analysis</li>
      <li>Text Analysis</li>
      <li>Operations Research</li>
      <li>Linear Optimization</li>
      <li>Data Mining</li>
    </ul>
  </div>
  
  <div class="skill-category">
    <h3 style="color: #e74c3c;">Data Visualization</h3>
    <ul>
      <li>Tableau (Certified Data Analyst)</li>
      <li>Matplotlib</li>
      <li>Plotly</li>
      <li>Streamlit</li>
      <li>Dashboard Design</li>
      <li>Interactive Visualizations</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #3498db;">Databases & Big Data</h3>
    <ul>
      <li>MySQL</li>
      <li>MongoDB</li>
      <li>NoSQL Databases</li>
      <li>Database Normalization</li>
      <li>Query Optimization</li>
      <li>Big Data Processing</li>
      <li>Data Warehouse Design</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #16a085;">Cloud & DevOps</h3>
    <ul>
      <li>AWS Cloud Services</li>
      <li>Cloud Computing</li>
      <li>Git Version Control</li>
      <li>Automated Pipelines</li>
      <li>Data Quality Monitoring</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #8e44ad;">Python Libraries</h3>
    <ul>
      <li>Pandas</li>
      <li>NumPy</li>
      <li>Scikit-Learn</li>
      <li>TensorFlow</li>
      <li>Matplotlib</li>
      <li>Anaconda</li>
      <li>pip</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #c0392b;">Business Tools</h3>
    <ul>
      <li>MS Office Suite</li>
      <li>Excel (Advanced)</li>
      <li>UML Modeling</li>
      <li>Project Management</li>
      <li>Technical Documentation</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3 style="color: #27ae60;">Specialized Skills</h3>
    <ul>
      <li>Geospatial Data Analysis</li>
      <li>Financial Fraud Detection</li>
      <li>Healthcare Analytics</li>
      <li>Remote Sensing</li>
      <li>OpenCV</li>
      <li>GenAI Applications</li>
    </ul>
  </div>

</div>

<h2>What Else</h2>

<p><b>Beyond the world of data and code：</b></p>  
  <div style="line-height: 1.5;">
  <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🏔️ I enjoy exploring beautiful trails, finding tranquility and perspective on weekend hiking adventures.</span></p>
  <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">📚 When indoors, I like reading books that expand my horizons—from data science literature to thought-provoking fiction.</span></p>
  <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🎮 I'm also an enthusiastic League of Legends player, where <i>strategic thinking</i> and <i>teamwork</i> offer a different kind of problem-solving challenge.</span></p>
  <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🍰 In my kitchen, you'll find me experimenting with baking techniques, applying the same precision and creativity that drives my professional work to create perfect pastries and breads.</span></p>
</div>

<br>

<div class="dog-section">
  <div class="dog-text" style="line-height: 1.5;">
      <p><b>My constant companion on life's adventures is:</b></p>
      <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🐕 Wangwang Shen, my beloved dog! </span></p>
      <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">✈️ He made the incredible journey with me from China to the USA.</span></p>
      <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🦋 Wangwang's curiosity and joy remind me to appreciate the simple pleasures and find wonder in our surroundings, <i>no matter how busy</i> life gets.</span></p>
      <p style="margin: 0.5rem 0;"><span style="margin-left: 20px;">🌈 We really enjoy the US's friendly pet-environment.</span></p>
    <p style="margin: 2rem 0;"><b>To pet him and enjoy his fluffy tail,</b> <strong class="hire-me">HIRE ME!</strong></p>
  </div>
  
  <div class="dog-image">
    <img src="{{ '/assets/img/ww_tail.GIF' | relative_url }}" alt="Wangwang Shen">
  </div>
</div>



<h2>Contact</h2>

Feel free to reach out to me at [yanna.cshen@gmail.com](mailto:yanna.cshen@gmail.com) or connect with me on <a href="https://www.linkedin.com/in/chengyang-shen" target="_blank" onclick="event.stopPropagation();">LinkedIn</a> and <a href="https://github.com/YannaCS" target="_blank" onclick="event.stopPropagation();">GitHub</a>. You can also access to the above links and <a href="https://yannacs.github.io/assets/resume.pdf" target="_blank" onclick="event.stopPropagation();"><b>download my resume</b></a> from side bar.  


I'm here to help transform your data into **valuable insights and profit!**


<script type="text/javascript">
window.flipCard = function(element) {
  if (!element) return;
  if (element.classList.contains('no-flip')) return;
  
  element.classList.toggle('flipped');
  
  document.querySelectorAll('.timeline-content').forEach(function(item) {
    if (item !== element && item.classList.contains('flipped')) {
      item.classList.remove('flipped');
    }
  });
}
</script>

