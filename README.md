<div align="center">
 <img src="assets/img/logo.png" alt="logo" width="200px"> 
<h1> Mono2Stereo: A Benchmark and Empirical Study for Stereo Conversion </h1>
 <a href='https://arxiv.org/abs/2503.22262'><img src='https://img.shields.io/badge/arXiv-2503.22262-b31b1b.svg'></a> &nbsp;
 <a href='https://github.com/song2yu/Mono2Stereo'><img src='https://img.shields.io/badge/Project-Page-Green'></a> &nbsp;
  <a href='https://huggingface.co/Two-hot/Mono2Stereo/tree/main'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Demo-blue'></a> &nbsp;
</div>

<div align="center">
<a href="https://song2yu.github.io/"><sup>1</sup>Songsong Yu</a> |
<a href="https://scholar.google.com/citations?hl=zh-CN&user=dEm4OKAAAAAJ&view_op=list_works"><sup>2</sup> Yuxin Chen<sup>🌟</sup></a> |
 <a href="https://scholar.google.com/citations?user=zJvrrusAAAAJ&hl=zh-CN&oi=ao"><sup>2</sup>Zhongang Qi<sup>📜 </sup></a> |
<a href="https://scholar.google.com/citations?user=ysXmZCMAAAAJ&hl=zh-CN&oi=ao"><sup>3</sup>Zeke Xie</a> |
<a href="https://scholar.google.com/citations?user=j1XFhSoAAAAJ&hl=zh-CN&oi=ao"><sup>1</sup>Yifan Wang</a> |
<a href="https://scholar.google.com/citations?user=EfTwkXMolscC&hl=zh-CN&oi=ao"><sup>1</sup>Lijun Wang<sup>📜 </sup></a> |
<a href="https://scholar.google.com/citations?user=4oXBp9UAAAAJ&hl=zh-CN&oi=ao"><sup>2</sup>Ying Shan</a> |
<a href="https://scholar.google.com/citations?user=D3nE0agAAAAJ&hl=zh-CN&oi=ao"><sup>1</sup>Huchuan Lu</a>
<br><br>
<sup>1</sup>Dalian University of Technology 
<sup>2</sup>ARC Lab, Tencent PCG
<sup>3</sup>The Hong Kong University of Science and Technology (Guangzhou)
</div>
<div align="center">
CVPR 2025
<sup>🌟</sup>Project Lead
<sup>📜 </sup>Corresponding Author
</div>



<div align="center">
<h2><p style="font-family: 'New Roman', Times, serif;font-size: 32px;">
🔆 Brief introduction </p>
</h2>
 </div>



<div align="left">
 <p style="font-family: 'New Roman', Times, serif;font-size: 22px;"> <strong>💡 Abstract.</strong> With the rapid proliferation of 3D devices and the shortage of 3D content, stereo conversion is attracting increasing attention. Recent works introduce pretrained Diffusion Models (DMs) into this task. However, due to the scarcity of large-scale training data and comprehensive benchmarks, the optimal methodologies for employing DMs in stereo conversion and the accurate evaluation of stereo effects remain largely unexplored. In this work, we introduce the Mono2Stereo dataset, providing high-quality training data and benchmark to support in-depth exploration of stereo conversion. With this dataset, we conduct an empirical study that yields two primary findings. 1) The differences between the left and right views are subtle, yet existing metrics consider overall pixels, failing to concentrate on regions critical to stereo effects. 2) Mainstream methods adopt either one-stage left-to-right generation or warp-and-inpaint pipeline, facing challenges of degraded stereo effect and image distortion respectively. Based on these findings, we introduce a new evaluation metric, Stereo Intersection-over-Union, which prioritizes disparity and achieves a high correlation with human judgments on stereo effect. Moreover, we propose a strong baseline model, harmonizing the stereo effect and image quality simultaneously, and notably surpassing current mainstream methods.</p>
</div>
 <br><br>

<img src="assets/img/teaser.png" alt="teaser" width="900px"> 
<div align="left">
 <br>
 <p style="font-family: 'New Roman', Times, serif;font-size: 22px;">
  <strong> 📦 Datasets.</strong> We collect approximately two million stereo image pairs for model training and provide the code for data processing. </p>

 <br><br>
</div>


<img src="assets/img/training.jpg" alt="pipe" width="900px">
<div align="left">
 <p style="font-family: 'New Roman', Times, serif;font-size: 22px;">
<strong>⛩️ Architecture.</strong> We find that due to the small differences between the left and right images, the model tends to degenerate into an identity mapping during training. Therefore, we add an edge consistency loss to force the model to focus on edge information. </p>
 <br><br>
</div>


<img src="assets/img/difference.png" alt="siou" width="900px">
<div align="left">
 <p style="font-family: 'New Roman', Times, serif;font-size: 22px;"> <strong>🧪 SIoU.</strong> We find that due to the small differences between the left and right images, the model tends to degenerate into an identity mapping during training. Therefore, we add an edge consistency loss to force the model to focus on edge information.</p>
 
 <br><br>
</div>



<div align="center">
<h2><p style="font-family: 'New Roman', Times, serif;font-size: 32px;">
🎥 Visual Effects </p>
</h2>
 <br>
 </div>
 
<div align="left">
<p style="font-family: 'New Roman', Times, serif;font-size: 22px;"> 👓 You can wear red-blue glasses to get the out-of-screen effect. 👓</p>
</div>
<br>
<img src="assets/img/Buddha.jpg" alt="Buddha" width="900px">
<img src="assets/img/wukong.jpg" alt="wukong" width="900px">
<img src="assets/img/wukong1.jpg" alt="wukong1" width="900px">
<img src="assets/img/sora.jpg" alt="sora" width="900px">
<img src="assets/img/seed.jpg" alt="demo" width="900px">

<br>
<div align="center">
<h2><p style="font-family: 'New Roman', Times, serif;font-size: 32px;">
🔥 Exploring the Future </p>
</h2>
 <br>
 </div>

<div align="left">
<p style="font-family: 'New Roman', Times, serif;font-size: 22px;">📢 It is important to note that our baseline model does not incorporate temporal information. Although it processes the input video frame by frame, the temporal consistency is not well-maintained, leading to flickering artifacts. In future work, we plan to train a video generation model specifically for stereo conversion tasks. The left panel shows the left-eye view, while the right panel displays the right-eye view generated by our baseline model.</p>
</div>

<video width="100%" controls>
  <source src="assets/img/video.mp4" type="video/mp4">
</video>



<section class="hero teaser" id="🎓 BibTeX">
    <div class="hero-body">
        <div class="column is-three-fifths" style=" margin-top: 30px; margin-bottom: 20px;">
            <h2 class="title is-3">BibTeX</h2>
            <pre><code>
            @misc{yu2025mono2stereobenchmarkempiricalstudy,
              title={Mono2Stereo: A Benchmark and Empirical Study for Stereo Conversion}, 
              author={Songsong Yu and Yuxin Chen and Zhongang Qi and Zeke Xie and Yifan Wang and Lijun Wang and Ying Shan and Huchuan Lu},
              year={2025},
              eprint={2503.22262},
              archivePrefix={arXiv},
              primaryClass={cs.CV},
              url={https://arxiv.org/abs/2503.22262}, 
             }
            </code></pre>
        </div>
    </div>
</section>


<div align="center">
<h2>
 <p style="font-family: 'New Roman', Times, serif;font-size: 32px;"> Acknowledgements</p>

</h2>
 <br>
 </div>
 
<div align="center">
Website adapted from the following <a href="https://github.com/CaiJimmy/hugo-theme-stack-starter">template</a>.
</div>


