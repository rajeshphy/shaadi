---
layout: default
title: Rajesh & Akansha Wedding Album
---

<div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 2rem; margin: 2rem 0;">
  
  <div style="text-align: center;">
    <img src="/shaadi/assets/Couple.JPG" alt="Rajesh" style="width: 160px; height: 160px; border-radius: 50%; box-shadow: 0 0 10px rgba(0,0,0,0.2); object-fit: cover;">
    <div style="margin-top: 0.5rem; font-weight: bold;">Akansha 💖 Rajesh</div>
    <div style="font-size: 0.9rem; color: #666;">A Journey of Love, Laughter & Forever 📷 </div>
  </div>
</div>

### 📸 Click an Album

<div id="album-buttons">
  <button onclick="filterByFolder('Chekka')">Chekka</button>
  <button onclick="filterByFolder('Shaadi')">Shaadi</button>
  <button onclick="filterByFolder('Recep')">Recep</button>
  <button onclick="filterByFolder('Single')">Single</button>
</div>

<div style="text-align: center; font-size: 0.95rem; margin-top: 1rem; line-height: 1.2;">
  <strong>Chekka</strong> – 22 April 2025<br>
  🌼 <strong>Lagan Bandhi & Haldi</strong> – May 9, 2025<br>
  💅 <strong>Mehandi & Sangeet</strong> – May 10, 2025<br>
  💍 <strong>Wedding</strong> – May 11, 2025<br>
  🎉 <strong>Reception</strong> – May 13, 2025
</div>
---

<div class="gallery" id="portrait-gallery"></div>

<div class="gallery" id="landscape-gallery"></div>

<script>
const allFiles = [
  { path: "/assets/Single/R/r_DSC_7120.JPG", name: "r_DSC_7120.JPG" },
  { path: "/assets/Single/R/r_DSC_7123.JPG", name: "r_DSC_7123.JPG" },
  { path: "/assets/Single/R/r_DSC_7119.JPG", name: "r_DSC_7119.JPG" },
  { path: "/assets/Single/R/r_DSC_7125.JPG", name: "r_DSC_7125.JPG" },
  { path: "/assets/Single/R/r_DSC_7118.JPG", name: "r_DSC_7118.JPG" },
  { path: "/assets/Single/R/r_DSC_6961.JPG", name: "r_DSC_6961.JPG" },
  { path: "/assets/Single/R/r_DSC_6963.JPG", name: "r_DSC_6963.JPG" },
  { path: "/assets/Single/R/r_DSC_7116.JPG", name: "r_DSC_7116.JPG" },
  { path: "/assets/Single/R/r_DSC_7117.JPG", name: "r_DSC_7117.JPG" },
  { path: "/assets/Single/R/r_DSC_6962.JPG", name: "r_DSC_6962.JPG" },
  { path: "/assets/Single/R/r_DSC_7112.JPG", name: "r_DSC_7112.JPG" },
  { path: "/assets/Single/R/r_DSC_7110.JPG", name: "r_DSC_7110.JPG" },
  { path: "/assets/Single/R/r_DSC_7111.JPG", name: "r_DSC_7111.JPG" },
  { path: "/assets/Single/A/r_DSC_7619.JPG", name: "r_DSC_7619.JPG" },
  { path: "/assets/Single/A/r_DSC_7583.JPG", name: "r_DSC_7583.JPG" },
  { path: "/assets/Single/A/r_DSC_7581.JPG", name: "r_DSC_7581.JPG" },
  { path: "/assets/Single/A/r_DSC_6969.JPG", name: "r_DSC_6969.JPG" },
  { path: "/assets/Single/A/r_DSC_7243.JPG", name: "r_DSC_7243.JPG" },
  { path: "/assets/Single/A/r_DSC_7241.JPG", name: "r_DSC_7241.JPG" },
  { path: "/assets/Single/A/r_DSC_7126.JPG", name: "r_DSC_7126.JPG" },
  { path: "/assets/Single/A/r_DSC_7131.JPG", name: "r_DSC_7131.JPG" },
  { path: "/assets/Single/A/r_DSC_7130.JPG", name: "r_DSC_7130.JPG" },
  { path: "/assets/Single/A/r_DSC_7129.JPG", name: "r_DSC_7129.JPG" },
  { path: "/assets/Single/A/r_DSC_7249.JPG", name: "r_DSC_7249.JPG" },
  { path: "/assets/Single/A/r_DSC_7488.JPG", name: "r_DSC_7488.JPG" },
  { path: "/assets/Single/A/r_DSC_7604.JPG", name: "r_DSC_7604.JPG" },
  { path: "/assets/Single/A/r_DSC_7610.JPG", name: "r_DSC_7610.JPG" },
  { path: "/assets/Single/A/r_DSC_7559.JPG", name: "r_DSC_7559.JPG" },
  { path: "/assets/Single/A/r_DSC_7612.JPG", name: "r_DSC_7612.JPG" },
  { path: "/assets/Single/A/r_DSC_7570.JPG", name: "r_DSC_7570.JPG" },
  { path: "/assets/Single/A/r_DSC_7564.JPG", name: "r_DSC_7564.JPG" },
  { path: "/assets/Single/A/r_DSC_7575.JPG", name: "r_DSC_7575.JPG" },
  { path: "/assets/Single/A/r_DSC_7588.JPG", name: "r_DSC_7588.JPG" },
  { path: "/assets/Single/A/r_DSC_7601.JPG", name: "r_DSC_7601.JPG" },
  { path: "/assets/Single/A/r_DSC_7600.JPG", name: "r_DSC_7600.JPG" },
  { path: "/assets/Single/A/r_DSC_7562.JPG", name: "r_DSC_7562.JPG" },
  { path: "/assets/Single/A/r_DSC_7576.JPG", name: "r_DSC_7576.JPG" },
  { path: "/assets/Single/A/r_DSC_7589.JPG", name: "r_DSC_7589.JPG" },
  { path: "/assets/Recep/r_DSC_7382.JPG", name: "r_DSC_7382.JPG" },
  { path: "/assets/Recep/r_DSC_7546.JPG", name: "r_DSC_7546.JPG" },
  { path: "/assets/Recep/r_DSC_7552.JPG", name: "r_DSC_7552.JPG" },
  { path: "/assets/Recep/r_DSC_7424.JPG", name: "r_DSC_7424.JPG" },
  { path: "/assets/Recep/r_DSC_7626.JPG", name: "r_DSC_7626.JPG" },
  { path: "/assets/Recep/r_DSC_7780.JPG", name: "r_DSC_7780.JPG" },
  { path: "/assets/Recep/r_DSC_7743.JPG", name: "r_DSC_7743.JPG" },
  { path: "/assets/Recep/r_DSC_7637.JPG", name: "r_DSC_7637.JPG" },
  { path: "/assets/Recep/r_DSC_7434.JPG", name: "r_DSC_7434.JPG" },
  { path: "/assets/Recep/r_DSC_7754.JPG", name: "r_DSC_7754.JPG" },
  { path: "/assets/Recep/r_DSC_7635.JPG", name: "r_DSC_7635.JPG" },
  { path: "/assets/Recep/r_DSC_7423.JPG", name: "r_DSC_7423.JPG" },
  { path: "/assets/Recep/r_DSC_7543.JPG", name: "r_DSC_7543.JPG" },
  { path: "/assets/Recep/r_DSC_7524.JPG", name: "r_DSC_7524.JPG" },
  { path: "/assets/Recep/r_DSC_7493.JPG", name: "r_DSC_7493.JPG" },
  { path: "/assets/Recep/r_DSC_7478.JPG", name: "r_DSC_7478.JPG" },
  { path: "/assets/Recep/r_DSC_7691.JPG", name: "r_DSC_7691.JPG" },
  { path: "/assets/Recep/r_DSC_7492.JPG", name: "r_DSC_7492.JPG" },
  { path: "/assets/Recep/r_DSC_7519.JPG", name: "r_DSC_7519.JPG" },
  { path: "/assets/Recep/r_DSC_7525.JPG", name: "r_DSC_7525.JPG" },
  { path: "/assets/Recep/r_DSC_7531.JPG", name: "r_DSC_7531.JPG" },
  { path: "/assets/Recep/r_DSC_7719.JPG", name: "r_DSC_7719.JPG" },
  { path: "/assets/Recep/r_DSC_7484.JPG", name: "r_DSC_7484.JPG" },
  { path: "/assets/Recep/r_DSC_7651.JPG", name: "r_DSC_7651.JPG" },
  { path: "/assets/Recep/r_DSC_7645.JPG", name: "r_DSC_7645.JPG" },
  { path: "/assets/Recep/r_DSC_7708.JPG", name: "r_DSC_7708.JPG" },
  { path: "/assets/Recep/r_DSC_7481.JPG", name: "r_DSC_7481.JPG" },
  { path: "/assets/Recep/r_DSC_7683.JPG", name: "r_DSC_7683.JPG" },
  { path: "/assets/Recep/r_DSC_7494.JPG", name: "r_DSC_7494.JPG" },
  { path: "/assets/Recep/r_DSC_7537.JPG", name: "r_DSC_7537.JPG" },
  { path: "/assets/Recep/r_DSC_7521.JPG", name: "r_DSC_7521.JPG" },
  { path: "/assets/Recep/r_DSC_7695.JPG", name: "r_DSC_7695.JPG" },
  { path: "/assets/Recep/r_DSC_7440.JPG", name: "r_DSC_7440.JPG" },
  { path: "/assets/Recep/r_DSC_7722.JPG", name: "r_DSC_7722.JPG" },
  { path: "/assets/Recep/r_DSC_7736.JPG", name: "r_DSC_7736.JPG" },
  { path: "/assets/Recep/r_DSC_7539.JPG", name: "r_DSC_7539.JPG" },
  { path: "/assets/Recep/r_DSC_7666.JPG", name: "r_DSC_7666.JPG" },
  { path: "/assets/Recep/r_DSC_7699.JPG", name: "r_DSC_7699.JPG" },
  { path: "/assets/Recep/r_DSC_7458.JPG", name: "r_DSC_7458.JPG" },
  { path: "/assets/Recep/r_DSC_7504.JPG", name: "r_DSC_7504.JPG" },
  { path: "/assets/Recep/r_DSC_7706.JPG", name: "r_DSC_7706.JPG" },
  { path: "/assets/Recep/r_DSC_7712.JPG", name: "r_DSC_7712.JPG" },
  { path: "/assets/Recep/r_DSC_7704.JPG", name: "r_DSC_7704.JPG" },
  { path: "/assets/Recep/r_DSC_7710.JPG", name: "r_DSC_7710.JPG" },
  { path: "/assets/Recep/r_DSC_7738.JPG", name: "r_DSC_7738.JPG" },
  { path: "/assets/Recep/r_DSC_7467.JPG", name: "r_DSC_7467.JPG" },
  { path: "/assets/Recep/r_DSC_7498.JPG", name: "r_DSC_7498.JPG" },
  { path: "/assets/Recep/r_DSC_7513.JPG", name: "r_DSC_7513.JPG" },
  { path: "/assets/Recep/r_DSC_7715.JPG", name: "r_DSC_7715.JPG" },
  { path: "/assets/Recep/r_DSC_7463.JPG", name: "r_DSC_7463.JPG" },
  { path: "/assets/Recep/r_DSC_7516.JPG", name: "r_DSC_7516.JPG" },
  { path: "/assets/Recep/r_DSC_7714.JPG", name: "r_DSC_7714.JPG" },
  { path: "/assets/Recep/r_DSC_7700.JPG", name: "r_DSC_7700.JPG" },
  { path: "/assets/Recep/r_DSC_7689.JPG", name: "r_DSC_7689.JPG" },
  { path: "/assets/Recep/r_DSC_7475.JPG", name: "r_DSC_7475.JPG" },
  { path: "/assets/Recep/r_DSC_7529.JPG", name: "r_DSC_7529.JPG" },
  { path: "/assets/Recep/r_DSC_7764.JPG", name: "r_DSC_7764.JPG" },
  { path: "/assets/Recep/r_DSC_7412.JPG", name: "r_DSC_7412.JPG" },
  { path: "/assets/Recep/r_DSC_7767.JPG", name: "r_DSC_7767.JPG" },
  { path: "/assets/Recep/r_DSC_7439.JPG", name: "r_DSC_7439.JPG" },
  { path: "/assets/Recep/r_DSC_7376.JPG", name: "r_DSC_7376.JPG" },
  { path: "/assets/Recep/r_DSC_7410.JPG", name: "r_DSC_7410.JPG" },
  { path: "/assets/Recep/r_DSC_7372.JPG", name: "r_DSC_7372.JPG" },
  { path: "/assets/Recep/r_DSC_7616.JPG", name: "r_DSC_7616.JPG" },
  { path: "/assets/Recep/r_DSC_7401.JPG", name: "r_DSC_7401.JPG" },
  { path: "/assets/Recep/r_DSC_7415.JPG", name: "r_DSC_7415.JPG" },
  { path: "/assets/Recep/r_DSC_7629.JPG", name: "r_DSC_7629.JPG" },
  { path: "/assets/Chekka/r_DSC_3225.JPG", name: "r_DSC_3225.JPG" },
  { path: "/assets/Chekka/r_DSC_3208.JPG", name: "r_DSC_3208.JPG" },
  { path: "/assets/Chekka/r_DSC_3143.JPG", name: "r_DSC_3143.JPG" },
  { path: "/assets/Chekka/r_DSC_3221.JPG", name: "r_DSC_3221.JPG" },
  { path: "/assets/Chekka/r_DSC_3154.JPG", name: "r_DSC_3154.JPG" },
  { path: "/assets/Chekka/r_DSC_3197.JPG", name: "r_DSC_3197.JPG" },
  { path: "/assets/Chekka/r_DSC_3206.JPG", name: "r_DSC_3206.JPG" },
  { path: "/assets/Chekka/r_DSC_3212.JPG", name: "r_DSC_3212.JPG" },
  { path: "/assets/Chekka/r_DSC_3189.JPG", name: "r_DSC_3189.JPG" },
  { path: "/assets/Chekka/r_DSC_3160.JPG", name: "r_DSC_3160.JPG" },
  { path: "/assets/Shaadi/r_DSC_7181.JPG", name: "r_DSC_7181.JPG" },
  { path: "/assets/Shaadi/r_DSC_6658.JPG", name: "r_DSC_6658.JPG" },
  { path: "/assets/Shaadi/r_DSC_6894.JPG", name: "r_DSC_6894.JPG" },
  { path: "/assets/Shaadi/r_DSC_6882.JPG", name: "r_DSC_6882.JPG" },
  { path: "/assets/Shaadi/r_DSC_6896.JPG", name: "r_DSC_6896.JPG" },
  { path: "/assets/Shaadi/r_DSC_7236.JPG", name: "r_DSC_7236.JPG" },
  { path: "/assets/Shaadi/r_DSC_7342.JPG", name: "r_DSC_7342.JPG" },
  { path: "/assets/Shaadi/r_DSC_7168.JPG", name: "r_DSC_7168.JPG" },
  { path: "/assets/Shaadi/r_DSC_7025.JPG", name: "r_DSC_7025.JPG" },
  { path: "/assets/Shaadi/r_DSC_7151.JPG", name: "r_DSC_7151.JPG" },
  { path: "/assets/Shaadi/r_DSC_7187.JPG", name: "r_DSC_7187.JPG" },
  { path: "/assets/Shaadi/r_DSC_7226.JPG", name: "r_DSC_7226.JPG" },
  { path: "/assets/Shaadi/r_DSC_6879.JPG", name: "r_DSC_6879.JPG" },
  { path: "/assets/Shaadi/r_DSC_7026.JPG", name: "r_DSC_7026.JPG" },
  { path: "/assets/Shaadi/r_DSC_6890.JPG", name: "r_DSC_6890.JPG" },
  { path: "/assets/Shaadi/r_DSC_6933.JPG", name: "r_DSC_6933.JPG" },
  { path: "/assets/Shaadi/r_DSC_7147.JPG", name: "r_DSC_7147.JPG" },
  { path: "/assets/Shaadi/r_DSC_6846.JPG", name: "r_DSC_6846.JPG" },
  { path: "/assets/Shaadi/r_DSC_7054.JPG", name: "r_DSC_7054.JPG" },
  { path: "/assets/Shaadi/r_DSC_7242.JPG", name: "r_DSC_7242.JPG" },
  { path: "/assets/Shaadi/r_DSC_7109.JPG", name: "r_DSC_7109.JPG" },
  { path: "/assets/Shaadi/r_DSC_7069.JPG", name: "r_DSC_7069.JPG" },
  { path: "/assets/Shaadi/r_DSC_7080.JPG", name: "r_DSC_7080.JPG" },
  { path: "/assets/Shaadi/r_DSC_7094.JPG", name: "r_DSC_7094.JPG" },
  { path: "/assets/Shaadi/r_DSC_6995.JPG", name: "r_DSC_6995.JPG" },
  { path: "/assets/Shaadi/r_DSC_6823.JPG", name: "r_DSC_6823.JPG" },
  { path: "/assets/Shaadi/r_DSC_7085.JPG", name: "r_DSC_7085.JPG" },
  { path: "/assets/Shaadi/r_DSC_7046.JPG", name: "r_DSC_7046.JPG" },
  { path: "/assets/Shaadi/r_DSC_7052.JPG", name: "r_DSC_7052.JPG" },
  { path: "/assets/Shaadi/r_DSC_6953.JPG", name: "r_DSC_6953.JPG" },
  { path: "/assets/Shaadi/r_DSC_6749.JPG", name: "r_DSC_6749.JPG" },
  { path: "/assets/Shaadi/r_DSC_7292.JPG", name: "r_DSC_7292.JPG" },
  { path: "/assets/Shaadi/r_DSC_6826.JPG", name: "r_DSC_6826.JPG" },
  { path: "/assets/Shaadi/r_DSC_7092.JPG", name: "r_DSC_7092.JPG" },
  { path: "/assets/Shaadi/r_DSC_7326.JPG", name: "r_DSC_7326.JPG" },
  { path: "/assets/Shaadi/r_DSC_6762.JPG", name: "r_DSC_6762.JPG" },
  { path: "/assets/Shaadi/r_DSC_6945.JPG", name: "r_DSC_6945.JPG" },
  { path: "/assets/Shaadi/r_DSC_6948.JPG", name: "r_DSC_6948.JPG" },
  { path: "/assets/Shaadi/r_DSC_7100.JPG", name: "r_DSC_7100.JPG" },
  { path: "/assets/Shaadi/r_DSC_6752.JPG", name: "r_DSC_6752.JPG" },
  { path: "/assets/Shaadi/r_DSC_7089.JPG", name: "r_DSC_7089.JPG" },
  { path: "/assets/Shaadi/r_DSC_7076.JPG", name: "r_DSC_7076.JPG" },
  { path: "/assets/Shaadi/r_DSC_6793.JPG", name: "r_DSC_6793.JPG" },
  { path: "/assets/Shaadi/r_DSC_6778.JPG", name: "r_DSC_6778.JPG" },
  { path: "/assets/Shaadi/r_DSC_7098.JPG", name: "r_DSC_7098.JPG" },
  { path: "/assets/Shaadi/r_DSC_7067.JPG", name: "r_DSC_7067.JPG" },
  { path: "/assets/Shaadi/r_DSC_7107.JPG", name: "r_DSC_7107.JPG" },
  { path: "/assets/Shaadi/r_DSC_6967.JPG", name: "r_DSC_6967.JPG" },
  { path: "/assets/Shaadi/r_DSC_6813.JPG", name: "r_DSC_6813.JPG" },
  { path: "/assets/Shaadi/r_DSC_7072.JPG", name: "r_DSC_7072.JPG" },
  { path: "/assets/Shaadi/r_DSC_7099.JPG", name: "r_DSC_7099.JPG" },
  { path: "/assets/Shaadi/r_DSC_7058.JPG", name: "r_DSC_7058.JPG" },
  { path: "/assets/Shaadi/r_DSC_7064.JPG", name: "r_DSC_7064.JPG" },
  { path: "/assets/Shaadi/r_DSC_7104.JPG", name: "r_DSC_7104.JPG" },
  { path: "/assets/Shaadi/r_DSC_7105.JPG", name: "r_DSC_7105.JPG" },
  { path: "/assets/Shaadi/r_DSC_6757.JPG", name: "r_DSC_6757.JPG" },
  { path: "/assets/Shaadi/r_DSC_7065.JPG", name: "r_DSC_7065.JPG" },
  { path: "/assets/Shaadi/r_DSC_7071.JPG", name: "r_DSC_7071.JPG" },
  { path: "/assets/Shaadi/r_DSC_7016.JPG", name: "r_DSC_7016.JPG" },
  { path: "/assets/Shaadi/r_DSC_7002.JPG", name: "r_DSC_7002.JPG" },
  { path: "/assets/Shaadi/r_DSC_6863.JPG", name: "r_DSC_6863.JPG" },
  { path: "/assets/Shaadi/r_DSC_7214.JPG", name: "r_DSC_7214.JPG" },
  { path: "/assets/Shaadi/r_DSC_7361.JPG", name: "r_DSC_7361.JPG" },
  { path: "/assets/Shaadi/r_DSC_6876.JPG", name: "r_DSC_6876.JPG" },
  { path: "/assets/Shaadi/r_DSC_7607.JPG", name: "r_DSC_7607.JPG" },
  { path: "/assets/Shaadi/r_DSC_7362.JPG", name: "r_DSC_7362.JPG" },
  { path: "/assets/Shaadi/r_DSC_6929.JPG", name: "r_DSC_6929.JPG" },
  { path: "/assets/Shaadi/r_DSC_6901.JPG", name: "r_DSC_6901.JPG" },
  { path: "/assets/Shaadi/r_DSC_6861.JPG", name: "r_DSC_6861.JPG" },
  { path: "/assets/Shaadi/r_DSC_7028.JPG", name: "r_DSC_7028.JPG" },
  { path: "/assets/Shaadi/r_DSC_7206.JPG", name: "r_DSC_7206.JPG" },
  { path: "/assets/Shaadi/r_DSC_6939.JPG", name: "r_DSC_6939.JPG" },
  { path: "/assets/Shaadi/r_DSC_6905.JPG", name: "r_DSC_6905.JPG" },
  { path: "/assets/Shaadi/r_DSC_7171.JPG", name: "r_DSC_7171.JPG" },
  { path: "/assets/Shaadi/r_DSC_6872.JPG", name: "r_DSC_6872.JPG" },
  { path: "/assets/Shaadi/r_DSC_6912.JPG", name: "r_DSC_6912.JPG" },
  { path: "/assets/Shaadi/r_DSC_7166.JPG", name: "r_DSC_7166.JPG" },
  { path: "/assets/Shaadi/r_DSC_6668.JPG", name: "r_DSC_6668.JPG" },
  { path: "/assets/Shaadi/r_DSC_7012.JPG", name: "r_DSC_7012.JPG" },
];

  function clearGalleries() {
    document.getElementById("portrait-gallery").innerHTML = "";
    document.getElementById("landscape-gallery").innerHTML = "";
  }

  function filterByFolder(folder) {
    clearGalleries();

    const baseUrl = "{{ site.baseurl }}";


    const folderPath = "assets/" + folder + "/";

    const filteredFiles = allFiles.filter(file => file.path.startsWith("/" + folderPath));

    if (filteredFiles.length === 0) {
      alert("No images found in folder: " + folder);
      return;
    }

    filteredFiles.forEach(file => {
      const wrapper = document.createElement("div");
      wrapper.classList.add("photo-box");

      // Image with full-size on click
      const link = document.createElement("a");
      link.href = baseUrl + "/" +file.path;
      link.target = "_blank";

      const img = new Image();
      img.src = baseUrl + "/" +file.path;
      img.alt = file.name;
      img.classList.add("album-img");
      link.appendChild(img);

      // Download button
      const downloadBtn = document.createElement("a");
      downloadBtn.href = baseUrl + "/" +file.path;
      downloadBtn.download = file.name;
      downloadBtn.classList.add("download-button");
      downloadBtn.innerText = "⬇️ Download";

      // Add to wrapper
      wrapper.appendChild(link);
      wrapper.appendChild(downloadBtn);

      // Portrait or Landscape
      img.onload = function () {
        if (img.naturalWidth > img.naturalHeight) {
          document.getElementById("landscape-gallery").appendChild(wrapper);
        } else {
          document.getElementById("portrait-gallery").appendChild(wrapper);
        }
      };
    });
  }
</script>
