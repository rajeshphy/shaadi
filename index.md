---
layout: default
title: Rajesh & Akansha Wedding Album
---

# 💖 Rajesh & Akansha 💖

<div style="text-align: center; margin-top: -10px; font-size: 1.2rem; color: #666;">
  Together Forever — A Journey Captured in Moments
</div>

---

## 📂 Select Album

<div id="album-buttons">
  <button onclick="filterByFolder('Chekka')">Chekka</button>
  <button onclick="filterByFolder('Barat')">Barat</button>
  <button onclick="filterByFolder('Shaadi')">Shaadi</button>
  <button onclick="filterByFolder('Reception')">Reception</button>
  <button onclick="filterByFolder('Individual')">Individual</button>
</div>

---

## 🖼 Portrait Orientation
<div class="gallery" id="portrait-gallery"></div>

## 🖼 Landscape Orientation
<div class="gallery" id="landscape-gallery"></div>
<script>
const allFiles = [
  { path: "/assets/Individual/A/r_DSC_7126.JPG", name: "r_DSC_7126.JPG" },
  { path: "/assets/Individual/A/r_DSC_7131.JPG", name: "r_DSC_7131.JPG" },
  { path: "/assets/Individual/A/r_DSC_7130.JPG", name: "r_DSC_7130.JPG" },
  { path: "/assets/Individual/A/r_DSC_7129.JPG", name: "r_DSC_7129.JPG" },
  { path: "/assets/Individual/A/r_DSC_7249.JPG", name: "r_DSC_7249.JPG" },
  { path: "/assets/Individual/A/r_DSC_7488.JPG", name: "r_DSC_7488.JPG" },
  { path: "/assets/Individual/A/r_DSC_7604.JPG", name: "r_DSC_7604.JPG" },
  { path: "/assets/Individual/A/r_DSC_7610.JPG", name: "r_DSC_7610.JPG" },
  { path: "/assets/Individual/A/r_DSC_7559.JPG", name: "r_DSC_7559.JPG" },
  { path: "/assets/Individual/A/r_DSC_7612.JPG", name: "r_DSC_7612.JPG" },
  { path: "/assets/Individual/A/r_DSC_7570.JPG", name: "r_DSC_7570.JPG" },
  { path: "/assets/Individual/A/r_DSC_7564.JPG", name: "r_DSC_7564.JPG" },
  { path: "/assets/Individual/A/r_DSC_7575.JPG", name: "r_DSC_7575.JPG" },
  { path: "/assets/Individual/A/r_DSC_7588.JPG", name: "r_DSC_7588.JPG" },
  { path: "/assets/Individual/A/r_DSC_7601.JPG", name: "r_DSC_7601.JPG" },
  { path: "/assets/Individual/A/r_DSC_7600.JPG", name: "r_DSC_7600.JPG" },
  { path: "/assets/Individual/A/r_DSC_7562.JPG", name: "r_DSC_7562.JPG" },
  { path: "/assets/Individual/A/r_DSC_7576.JPG", name: "r_DSC_7576.JPG" },
  { path: "/assets/Individual/A/r_DSC_7589.JPG", name: "r_DSC_7589.JPG" },
];








  function clearGalleries() {
    document.getElementById("portrait-gallery").innerHTML = "";
    document.getElementById("landscape-gallery").innerHTML = "";
  }

  function filterByFolder(folder) {
    clearGalleries();

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
      link.href = file.path;
      link.target = "_blank";

      const img = new Image();
      img.src = file.path;
      img.alt = file.name;
      img.classList.add("album-img");
      link.appendChild(img);

      // Download button
      const downloadBtn = document.createElement("a");
      downloadBtn.href = file.path;
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