### **📄 README.md**  

This `README.md` provides an overview of the **Torch in R** tasks we have completed, including dataset handling, visualization, and machine learning model training.  

---

## **Project Overview**  
This project is focused on using the **Torch library in R** for deep learning tasks, including data processing, visualization, and training models. The tasks follow the **Google Summer of Code (GSoC) 2025 TorchVision in R Improvements** requirements.

---

## **Tasks Completed**  

### **Easy Task: Torch Installation & Visualization**
**Objective**: Install `torch`, load a dataset, and generate an **advanced visualization** using R Markdown (`easy.Rmd`).  

**Files Added**:  
- **easy.Rmd** – Generates an interactive **3D visualization** using `torch` and `plotly`.  

**What We Did**:  
- Installed **`torch`** and necessary dependencies.  
- Created a **3D surface plot** using `torch_linspace()`, `torch_meshgrid()`, and `plotly`.  
- Resolved **HTML output issues** by updating the **YAML settings** in `easy.Rmd`.  

**Run it using**:  
```r
rmarkdown::render("easy.Rmd")
```

---

### **Medium Task: Spam Dataset Processing & Model Training**
**Objective**: Load, preprocess, and train a model on the **Spam dataset** using `torch` in R.  

**Files Added**:  
- **medium.Rmd** – Implements **data loading, preprocessing, and neural network training**.  

**What We Did**:  
- Loaded the **Spam dataset** from UCI ML Repository.  
- Converted data to a **torch tensor**, applied **normalization**, and implemented a **custom dataset class** (`spam_dataset`).  
- Trained a **3-layer neural network** with:
  - **ReLU activation**  
  - **Dropout regularization**  
  - **Adam optimizer**  
- Ran **20 epochs**, tracked **loss reduction**, and verified results.

**Final Model Loss:**  
```
Epoch 20: Loss = 2.9134
```

**Run it using**:  
```r
rmarkdown::render("medium.Rmd")
```

---

### **Hard Task: Forking Torch & Adding Spam Dataset Loader**
[`Link to the fOrked Repository`](https://github.com/koshtiakanksha/torch/)
**Objective**: Fork the `torch` repository and add a **Spam dataset loader with tests and documentation**.  

**Files Added in Forked Repository**:
1. **Spam Dataset Loader (`spam_dataset.R`)**  
   **Location:** [`R/spam_dataset.R`](https://github.com/koshtiakanksha/torch/blob/main/R/spam_dataset.R)  
   - Defines the **Spam dataset loader** for Torch in R.  
   - Converts the dataset into **torch tensors** and supports **batch processing**.  

2. **Test File (`test_spam_dataset.R`)**  
   **Location:** [`tests/testthat/test_spam_dataset.R`](https://github.com/koshtiakanksha/torch/blob/main/tests/testthat/test_spam_dataset.R)  
   - Tests the dataset loader using **`testthat`**.  
   - Ensures the dataset loads properly and tensors are correctly formatted.  

3. **Documentation (`spam_dataset.Rd`)**  
   **Location:** [`man/spam_dataset.Rd`](https://github.com/koshtiakanksha/torch/blob/main/man/spam_dataset.Rd)  
   - Provides **function documentation** for `spam_dataset()`.  
   - Includes **usage examples** and dataset details.  

**Testing the Dataset Loader:**  
```r
testthat::test_dir("tests/testthat")
```
**Test Results:**
```
[ FAIL 0 | WARN 0 | SKIP 0 | PASS 3 ]
```
**All tests passed successfully!**  
