---
layout: page
title: Portfolio
permalink: /portfolio/
---

<style>
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px;
  margin-top: 2rem;
}
.portfolio-card {
  border: 1px solid #ddd;
  border-radius: 12px;
  overflow: hidden;
  background-color: #fff;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  transition: transform 0.2s ease;
}
.portfolio-card:hover {
  transform: translateY(-4px);
}
.portfolio-card img {
  width: 100%;
  height: auto;
  display: block;
}
.portfolio-card-content {
  padding: 1rem;
}
.portfolio-card h3 {
  margin-top: 0;
}
.portfolio-card a {
  text-decoration: none;
  font-weight: bold;
  color: #007acc;
}
.portfolio-card a:hover {
  text-decoration: underline;
}
</style>

## Portfolio Projects

<div class="portfolio-grid">

  <div class="portfolio-card">
    <img src="/assets/landfill_model.png" alt="Landfill model">
    <div class="portfolio-card-content">
      <h3>Landfill Site Suitability Modeling</h3>
      <p>Developed a GIS-based MCDA model to identify optimal landfill sites using slope, land cover, roads, and hydrology layers.</p>
      <a href="/assets/Landfill-Site-Suitability-Model.pdf" target="_blank">View Full Report →</a>
    </div>
  </div>

  <!-- Add more cards below -->

</div>
