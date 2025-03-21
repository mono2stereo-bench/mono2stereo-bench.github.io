<div align="center">
 <img src="assets/img/logo.png" alt="logo" width="200px"> 
<h1> Mono2Stereo: A Benchmark and Empirical Study for Stereo Conversion </h1>
 <a href='https://arxiv.org/abs/2409.02095'><img src='https://img.shields.io/badge/arXiv-2409.02095-b31b1b.svg'></a> &nbsp;
 <a href='https://depthcrafter.github.io'><img src='https://img.shields.io/badge/Project-Page-Green'></a> &nbsp;
</div>

<div align="center">
<a href="https://song2yu.github.io/"><sup>1</sup>Songsong Yu</a> |
<a href="https://scholar.google.com/citations?hl=zh-CN&user=dEm4OKAAAAAJ&view_op=list_works"><sup>2</sup> Yuxin Chen</a> |
<a href="https://scholar.google.com/citations?user=ysXmZCMAAAAJ&hl=zh-CN&oi=ao"><sup>3</sup>Zeke Xie</a> |
<a href="https://scholar.google.com/citations?user=j1XFhSoAAAAJ&hl=zh-CN&oi=ao"><sup>1</sup>Yifan Wang</a> |
<a href="https://scholar.google.com/citations?user=EfTwkXMolscC&hl=zh-CN&oi=ao"><sup>1</sup>Lijun Wang</a> |
<a href="https://scholar.google.com/citations?user=zJvrrusAAAAJ&hl=zh-CN&oi=ao"><sup>2</sup>Zhongang Qi</a> |
<a href="https://scholar.google.com/citations?user=4oXBp9UAAAAJ&hl=zh-CN&oi=ao"><sup>2</sup>Ying Shan</a> |
<a href="https://scholar.google.com/citations?user=D3nE0agAAAAJ&hl=zh-CN&oi=ao"><sup>1</sup>Huchuan Lu</a>
<br><br>
<sup>1</sup>Dalian University of Technology 
<sup>2</sup>ARC Lab, Tencent PCG
<sup>3</sup>The Hong Kong University of Science and Technology (Guangzhou)
</div>
<div align="center">
CVPR 2025

</div>


<div align="center">
<h2>
 Brief introduction
</h2>
 <br>
 </div>

<div align="left">
<strong> Abstract.</strong> With the rapid proliferation of 3D devices and the shortage of 3D content, stereo conversion is attracting increasing attention. Recent works introduce pretrained Diffusion Models (DMs) into this task. However, due to the scarcity of large-scale training data and comprehensive benchmarks, the optimal methodologies for employing DMs in stereo conversion and the accurate evaluation of stereo effects remain largely unexplored. In this work, we introduce the Mono2Stereo dataset, providing high-quality training data and benchmark to support in-depth exploration of stereo conversion. With this dataset, we conduct an empirical study that yields two primary findings. 1) The differences between the left and right views are subtle, yet existing metrics consider overall pixels, failing to concentrate on regions critical to stereo effects. 2) Mainstream methods adopt either one-stage left-to-right generation or warp-and-inpaint pipeline, facing challenges of degraded stereo effect and image distortion respectively. Based on these findings, we introduce a new evaluation metric, Stereo Intersection-over-Union, which prioritizes disparity and achieves a high correlation with human judgments on stereo effect. Moreover, we propose a strong baseline model, harmonizing the stereo effect and image quality simultaneously, and notably surpassing current mainstream methods. Our code and data will be open-sourced to promote further research in stereo conversion.
 <br><br>
</div>

<img src="assets/img/teaser.png" alt="teaser" width="900px"> 
<div align="left">
 <br>
 <strong> Datasets.</strong> We collect approximately two million stereo image pairs for model training and provide the code for data processing.
 <br><br>
</div>


<img src="assets/img/training.jpg" alt="pipe" width="900px">
<div align="left">
 <strong> Architecture.</strong> We find that due to the small differences between the left and right images, the model tends to degenerate into an identity mapping during training. Therefore, we add an edge consistency loss to force the model to focus on edge information.
 <br><br>
</div>


<img src="assets/img/difference.png" alt="siou" width="900px">
<div align="left">
 <strong> SIoU.</strong> We find that due to the small differences between the left and right images, the model tends to degenerate into an identity mapping during training. Therefore, we add an edge consistency loss to force the model to focus on edge information.
 <br><br>
</div>



<div align="center">
<h2>
Visual Effects
</h2>
 <br>
 </div>

<img src="assets/img/Buddha.jpg" alt="siou" width="900px">
<img src="assets/img/wukong.jpg" alt="siou" width="900px">
<img src="assets/img/wukong1.jpg" alt="siou" width="900px">
<img src="assets/img/sora.jpg" alt="siou" width="900px">


<div align="center">
<h2>
BibTeX
</h2>
 <br>
 </div>
<div>
  <div contenteditable="false" style="border: 1px solid #ccc; padding: 10px; width: 300px; height: 100px; overflow: auto;">
    here is a statement.
  </div>
</div>


<div align="center">
<h2>
Acknowledgements
</h2>
 <br>
 </div>
 
<div align="center">
Website adapted from the following <a href="https://github.com/CaiJimmy/hugo-theme-stack-starter">template</a>.
</div>


