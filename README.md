
<!-- PROJECT SHIELDS -->
![image](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![image](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![image](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=Keras&logoColor=white)


<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="https://i.ibb.co/V2XG0Kt/logo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Minerals Rocks Image Classification</h3>
</div>


![](https://i.imgur.com/waxVImv.png)

<!-- ABOUT THE PROJECT -->
<h2 id="about-the-project"> :pencil: About The Project</h2>

<p align="justify"> The aim of the project is to create an image dataset of minerals and rocks and train a model for their classification.
    The images are recovered through web scraping and from personal collections. After having downloaded them, each category is checked by hand to eliminate any non-compliant images
    <br>
  <div align="center">
    <img src="https://i.ibb.co/GtHY2wk/cnn.png" alt="cnn" border="0"></a>
  </div>
</p>

![](https://i.imgur.com/waxVImv.png)
<!-- TODO -->

<h2 id="roadmap"> TODO:</h2>
  - Define a utils.py file with all reusable fucntions like plotting, load data.
  
![](https://i.imgur.com/waxVImv.png)

<!-- ROADMAP -->
<h2 id="roadmap"> :dart: Roadmap</h2>

- [ ] Creation of the dataset containing images of minerals and rocks (Working on). Source (Google, Bing, Mindat.org, Personal collection)
    - <details>
        <summary>Images recovered</summary>

        * olivine
        * pyrite
        * opal
        * quartz
        * biotite
        * muscovite
        * calcite
        * gypsum
        * fluorite
        * malachite
        * amazonite
        * tourmaline
        * azurite
        * bismuth
        * rhodochrosite
        * uvarovite
        * realgar
        * rutile
        * cuprite
        * manganit
        * chalcedony
        * corundum
        * celestite
        * smoky quartz
        * tiger eye stone
        * scolecite
        * crocoite
        * carnelia
      </details>
- [ ] Clean the dataset (working on). First partial cleaning,
- [ ] Train the model (python) and covert it for tensorflow js
- [ ] Image pre-processing 
- [ ] Data augmentation
- [ ] Model
    - [ ] Develop a baseline
    - [ ] Train the model
    - [ ] Hyperparameter tuning?
    - [ ] Converto it for tensorflow js
 - [ ] Develop Angular WebApp

![](https://i.imgur.com/waxVImv.png)

| Model Type                | Classes            | Description                                                                           |
|---------------------------|--------------------|---------------------------------------------------------------------------------------|
| CNN from scratch  model_1 | Quartz, Pyrite (2) | Start Simple - Build a custom CNN baseline model for a binary classification problem. |
| Fine - Tuning  model_2    | Quartz, Pyrite (2) | Take the weights of a pretrained model and fine-tune to my problem.                   |
| CNN from scratch  model_3 | 10                 | Same as model_1 but now its a multiclass problem                                      |
| Fine - Tuning  model_4    | 10                 | Same as model_2 but now its a multiclass problem                                      |

![](https://i.imgur.com/waxVImv.png)

<!-- Training on small dataset - Starting with a binary classification problem - Quartz Pyrite -->
<h2 id="trainingsmall"> 📁 Binary Classification Baseline Model (Model_1)</h2>
<h3 align="justify"> Model_1 Architecture</h3>
<br>
<p align="justify"> The first model is build from scratch.
This architecture uses 3x3 convolution filter, starting with 32 filter incrementing up to 256. Max pooling was applied over a 2x2 pixel window after every convolutional layer. No techniques are applied to reduce overfitting (Dropout, data augmentation).
Since i have a binary classification task, i use the binary crossentropy loss. As an optimizer, i use Adam optimizer. Then, i train (fit) the network with batch size 32 and 20 epochs.
No callback is uesed (Es. EarlyStopping).
</p> 
<img src="https://i.ibb.co/fGZ1X0v/model.png" alt="model_1_architecture" border="0"></img>
<br>
<h3 align="justify"> Model_1 Performance Plot</h3>
<br>
<img src="https://i.ibb.co/rHsLDGP/accuracy.png" alt="model_1_accuracy_loss_curves" border="0"></img>
<br>
<h3 align="justify"> Prediction plot (random images from google images)</h3>
<h4>Pyrite</h4>
<img src="https://i.ibb.co/cL7v2vS/pred-pir.png" alt="pred-pir" border="0"></img>
<br>
<h4>Quartz</h4>
<img src="https://i.ibb.co/SJqMHVN/pred-qz.png" alt="pred-qz" border="0"></img>
