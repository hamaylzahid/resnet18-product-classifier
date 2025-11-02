<h1 align="center">🖼️ ResNet18 Product Classifier</h1>
<h5 align="center">Classifying product images with Deep Learning</h5>

<p  align="center" style="color: #555; font-size: 16px;">
  A practical implementation of <strong>ResNet18</strong> for product image classification.<br>
  This project uses transfer learning to classify products across multiple categories,<br>
  validate model performance, and predict real-world images with high accuracy.
</p>

<!-- 🔧 Core Technology Stack -->
<h4 align="center">🔧 Core Technology Stack</h4>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python&logoColor=white" alt="Python Badge" />
  <img src="https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c?style=flat&logo=pytorch&logoColor=white" alt="PyTorch Badge" />
  <img src="https://img.shields.io/badge/Torchvision-ML-orange?style=flat&logo=opencv&logoColor=white" alt="Torchvision Badge" />
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?style=flat&logo=scikit-learn&logoColor=white" alt="Scikit-learn Badge" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=flat&logo=plotly&logoColor=white" alt="Matplotlib Badge" />
</p>

<!-- 📄 Project Info -->
<h4 align="center">📄 Project Info</h4>

<p align="center">
  <img src="https://img.shields.io/github/last-commit/hamaylzahid/resnet18-product-classifier?style=flat&color=orange&logo=github" alt="Last Commit Badge" />
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=flat&logo=vercel&logoColor=white" alt="Status Badge" />
</p>

<p align="center" style="color: #666; font-size: 15px;">
  🧩 Built to classify product images accurately – from training to real-world predictions.
</p>
---
<!-- Dataset Section -->
<div style="margin-top:30px;">
    <h2  align="center" style="text-align:center;">Dataset</h2>
    <p align="center">
        The model was trained and validated on the <strong>Ecommerce Product Images (18K)</strong> dataset 
        from Kaggle. This dataset contains 18,175 images categorized into <strong>9 major classes</strong> 
        representing products from various e-commerce platforms such as Amazon and Walmart.
    </p>
    <p align="center">
        Images are preprocessed to <strong>224×224 pixels</strong>, suitable for use with pre-trained CNN models. 
        The dataset is split into <strong>train</strong> and <strong>validation</strong> sets for model training, 
        with an additional <strong>check set</strong> reserved for visual evaluation during deployment.
    </p>
    <p align="center">
        The dataset was collected using web scraping techniques and enhanced with resources like the 
        Amazon Berkeley Objects (ABO) project. It provides a balanced and high-quality dataset for 
        multi-class product image classification tasks.
    </p>
    <p>
        <strong>License:</strong> Apache 2.0 &nbsp; | &nbsp; <strong>Total Images:</strong> 18,175 &nbsp; | &nbsp; <strong>Classes:</strong> 9
    </p>
    <p align="center"  style="text-align:center;">
    <a href="https://www.kaggle.com/datasets/fatih_kgg/ecommerce_product_images_18k" target="_blank">
        <img src="https://img.shields.io/badge/Kaggle-Dataset-blue?logo=kaggle&style=for-the-badge" 
             alt="Kaggle Dataset Badge">
    </a>
</p>

</div>
---
<hr style="border:1px solid #ccc; margin-top:20px; margin-bottom:20px;">

<h2 align="center">📖 Table of Contents</h2>

<ul style="list-style-type:none; font-size:16px; color:#444; text-align:center; line-height:2;">
  <li>🧠 <a href="#-project-overview">Project Overview</a></li>
  <li>🎯 <a href="#-core-objectives">Core Objectives</a></li>
  <li>🖼️ <a href="#-dataset-and-images">Dataset & Images</a></li>
  <li>🛠️ <a href="#system-architecture">System Architecture</a></li>
  <li>🧪 <a href="#-training-workflow">Training Workflow</a></li>
  <li>📊 <a href="#-evaluation--metrics">Evaluation & Metrics</a></li>
  <li>🔥 <a href="#-bias-handling">Bias Handling</a></li>
  <li>⚙️ <a href="#setup-installation">Setup & Installation</a></li>
  <li>🙏 <a href="#-acknowledgments">Acknowledgments</a></li>
  <li>💼 <a href="#-libraries--tools">Libraries & Tools</a></li>
  <li>🤝 <a href="#-contact--contribution">Contact & Contribution</a></li>
  <li>📜 <a href="#-license">License</a></li>
</ul>

<hr align="center"  style="border:1px solid #ccc; margin-top:20px; margin-bottom:20px;">

<h2 align="center">🧠 Project Overview</h2>

<p align="center">
  <strong>ResNet18 Product Classifier</strong> is a deep learning-based image classification system designed to automatically recognize and categorize products with high accuracy.
  Powered by <code>PyTorch</code> and <code>torchvision</code>, it leverages the ResNet18 architecture to extract robust features and deliver reliable predictions for real-world images.
</p>

<p align="center">
  From raw product images to actionable insights, this system classifies items into multiple categories with precision and efficiency, handling variations in lighting, background, and angles.
</p>


<p align="center">
  <em>It’s not just a model — it’s an end-to-end solution for automated product recognition and classification.</em>
</p>

<h2 align="center" id="core-objectives">🎯 Core Objectives</h2>
<ul>
  <li>Implement transfer learning with pre-trained ResNet18.</li>
  <li>Train a model to classify 9 product categories.</li>
  <li>Validate performance using classification metrics.</li>
  <li>Test predictions on real-world product images.</li>
  <li>Provide visualizations including loss curves and confusion matrices.</li>
</ul>

<h2 align="center" id="system-architecture">🛠️ System Architecture</h2>

<ul>
  <li>Load pre-trained ResNet18 model.</li>
  <li>Replace the final layer with 9 output classes.</li>
  <li>Freeze base layers, fine-tune classification head.</li>
  <li>Train with CrossEntropyLoss and SGD optimizer.</li>
  <li>Evaluate and predict on validation and real-world images.</li>
</ul>

<h2 align="center"  id="training-workflow">🧪 Training Workflow</h2>
<ul>
  <li>Dataset: Images across 9 product categories.</li>
  <li>Preprocessing: Resize, normalize, and apply Torchvision transforms.</li>
  <li>Training: Fine-tune top layers for 20 epochs.</li>
  <li>Validation: Confusion matrix, accuracy, classification report.</li>
  <li>Real-world Testing: Classify unseen product images.</li>
</ul>

---

<h2 align="center" id="evaluation-metrics">📊 Evaluation & Metrics</h2>

<ul style="text-align:left; margin-left:40px;">
    <li>Precision, Recall, F1-Score: High across all 9 categories</li>
    <li>Real-World Predictions: Correctly classified unseen images</li>
</ul>

<!-- Confusion Matrix -->
<div align="center"  style="text-align:center; margin-top:20px;">
    <h3 align="center">Confusion Matrix</h3>
    <img src="https://github.com/hamaylzahid/resnet18-product-classifier/blob/main/confusion matrix.png?raw=true" 
         alt="Confusion Matrix" width="600">
</div>

<hr align="center" style="margin:40px 0; border:1px solid #ccc;">

<!-- Validation Curve -->
<div align="center" style="text-align:center; margin-top:20px;">
    <h3>Validation Predictions</h3>
    <img src="https://github.com/hamaylzahid/resnet18-product-classifier/blob/main/trainingvsvalidation_accuracy.png?raw=true" 
         alt="Validation Predictions" width="600">
</div>


<h2 align="center" id="bias-handling">🔥 Bias Handling</h2>
<ul>
  <li>Balanced dataset across all classes.</li>
  <li>Data augmentation applied to reduce overfitting.</li>
  <li>Ensures robust predictions on unseen data.</li>
</ul>

---

<!-- Real-World Predictions & Results -->
<div style="text-align:center;">
    <h2 align="center">🖼️ Real-World Predictions & Results</h2>
    <p align="center">
      The ResNet18 Product Classifier was tested on real-world product images to demonstrate its practical performance. 
      Below are the prediction images and the corresponding results summary.
    </p>
</div>
<h3 style="text-align:center;">Real-World Predictions</h3>
<div align="center style="text-align:center;">
    <img src="https://github.com/hamaylzahid/resnet18-product-classifier/blob/main/real%20world%20imgpred.png?raw=true" 
         alt="Real World Predictions" width="600">
</div>

<h3 style="text-align:center;">Real-World Prediction Results</h3>
<div align="center style="text-align:center;">
    <img src="https://github.com/hamaylzahid/resnet18-product-classifier/blob/main/results.png?raw=true" 
         alt="Real World Prediction Results" width="600">
</div>

<h2 align="center" id="setup-installation">⚙️ Setup & Installation</h2>

<pre>
# Clone repository
git clone https://github.com/hamaylzahid/resnet18-product-classifier.git

# Navigate to folder
cd resnet18-product-classifier

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook resnet18-product-classifier.ipynb
</pre>
---
<p align="center">
  <em>💡 “Inspired by vision research. Powered by open knowledge.”</em>
</p>

<br>
<h2 align="center">💼 Libraries & Tools</h2><br>

<p align="center">
  The <strong>ResNet18 Product Classifier</strong> leverages a modern deep learning ecosystem — optimized, scalable, and research-ready.
</p>

<p align="center">
  🧠 Every library was carefully chosen for specific tasks — from image preprocessing, model training, evaluation, to visualization.<br>
  🔗 Together, they create a seamless end-to-end pipeline for accurate product classification in real-world scenarios.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-Deep%20Learning-red?style=flat-square&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Torchvision-Pretrained%20Models-orange?style=flat-square&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-Data%20Handling-blue?style=flat-square&logo=pandas" />
  <img src="https://img.shields.io/badge/Numpy-Numerical%20Ops-informational?style=flat-square&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-green?style=flat-square&logo=matplotlib" />
  <img src="https://img.shields.io/badge/Scikit--Learn-Evaluation-orange?style=flat-square&logo=scikitlearn&logoColor=white" />
</p>

<br>
<h2 align="center">🤝 Contact & Contribution</h2><br>

<p align="center">
  Have feedback, want to collaborate, or just say hello?<br>
  <strong>Let’s connect and enhance product classification together.</strong>
</p>

<p align="center">
  📬 <a href="mailto:maylzahid588@gmail.com">maylzahid588@gmail.com</a> &nbsp; | &nbsp;
  💼 <a href="https://www.linkedin.com/in/your-linkedin-profile">LinkedIn Profile</a> &nbsp; | &nbsp;
  🌐 <a href="https://github.com/hamaylzahid/resnet18-product-classifier">GitHub Repo</a>
</p>

<p align="center">
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier/stargazers">
    <img src="https://img.shields.io/badge/Star%20This%20Project-Give%20a%20Star-yellow?style=for-the-badge&logo=github" alt="Star Badge" />
  </a>
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier/pulls">
    <img src="https://img.shields.io/badge/Contribute-Pull%20Requests%20Welcome-2ea44f?style=for-the-badge&logo=github" alt="PRs Welcome Badge" />
  </a>
</p>

<p align="center">
  ⭐ Found this project helpful? Give it a star on GitHub!<br>
  🤝 Want to improve it? Submit a PR and join the mission.<br>
  <sub><i>Your contributions help enhance real-world product classification systems.</i></sub>
</p>

<br>
<h2 align="center">📜 License</h2><br>

<p align="center">
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier/commits/main">
    <img src="https://img.shields.io/github/last-commit/hamaylzahid/resnet18-product-classifier?color=blue" alt="Last Commit">
  </a>
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier">
    <img src="https://img.shields.io/github/repo-size/hamaylzahid/resnet18-product-classifier?color=lightgrey" alt="Repo Size">
  </a>
</p>

<p align="center">
  This project is licensed under the <strong>MIT License</strong> — open to use, modify, and expand.
</p>

<p align="center">
  ✅ <strong>Project Status:</strong> Complete & Portfolio-Ready<br>
  🧾 <strong>License:</strong> MIT — <a href="LICENSE">View License »</a>
</p>

<p align="center">
  <strong>Crafted with deep learning expertise & real-world vision applications</strong> 🖼️✨
</p>

<p align="center">
  <a href="https://github.com/hamaylzahid">
    <img src="https://img.shields.io/badge/GitHub-%40hamaylzahid-181717?style=flat-square&logo=github" alt="GitHub" />
  </a>
  •
  <a href="mailto:maylzahid588@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Me-red?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
  •
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier">
    <img src="https://img.shields.io/badge/Repo-Link-blueviolet?style=flat-square&logo=github" alt="Repo" />
  </a>
  <br>
  <a href="https://github.com/hamaylzahid/resnet18-product-classifier/fork">
    <img src="https://img.shields.io/badge/Fork%20This%20Project-Contribute%20to%20AI-2ea44f?style=flat-square&logo=github" alt="Fork Badge" />
  </a>
</p>

<p align="center">
  <sub><i>Designed for real-world product classification and deep learning showcase.</i></sub>
</p>

<p align="center">
  🤖 <b>Use this project to demonstrate your expertise in computer vision and AI</b><br>
  🧬 Clone it, modify it, expand it — and build real-world product classification solutions.
</p>
