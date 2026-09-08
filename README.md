# Source-Filter Analysis of Cross-disease Healthy vs Dysarthric Speech Classification in ALS and PD Using Matched and Mismatched Tasks
This repository provides official benchmark tables, demographic statistics, and evaluation metrics (mean F1 and accuracy $\pm$ SD) for **Amyotrophic Lateral Sclerosis (ALS)**, **Parkinson's Disease (PD)**, and **Healthy Controls (HC)** speech classification across 605 speakers (ALS: $54.21 \pm 12.10$ yrs, HC: $41.10 \pm 9.79$ yrs, PD: $57.12 \pm 9.99$ yrs). It evaluates cross-task (SPON, DIDK, IMG), cross-representation (Raw Wav, Source-Only, Filter-Only), and cross-disease model generalization.
> **Note on Reported Metrics:** While figures in the manuscript highlight primary Accuracy trends, all tables and linked datasets in this repository report both **Mean F1 score (sd)** and **Mean Accuracy (sd)** across 5 folds to ensure full transparency.

---

## 📂 Quick File Navigation & Mapping

Use the table below to navigate between the paper references and their exact source Excel files in this repository. 

| Paper Reference | Description & Evaluation Metrics | Repository Source File |
| :--- | :--- | :--- |
| **Section 3 / Table 1** | Native language and gender distribution ($N = 605$) | 📊 [`Language_and_Gender_Distribution.xlsx`](./Language_and_Gender_Distribution.xlsx) |
| **Fig. 4** | Matched & mismatched cross-dataset evaluation (**F1 & Accuracy**) | 📊 [`matched_&_mismatched_values.xlsx`](./matched_%26_mismatched_values.xlsx) |
| **Fig. 5** | Disease-specific vs. Cross-disease evaluation (**F1 & Accuracy**) | 📊 [`cross_disease_values.xlsx`](./cross_disease_values.xlsx) |

---

<details>
<summary><b>1. Browser Preview: Dataset & Demographic Statistics (Table 1)</b> (Click to expand)</summary>

<br>

> 📊 **Source Excel File:** [`Language_and_Gender_Distribution.xlsx`](./Language_and_Gender_Distribution.xlsx)

This table summarizes the language and gender distribution ($N = 605$) across the three speaker cohorts: **ALS**, **Healthy Controls (HC)**, and **Parkinson's Disease (PD)**.

### Table 1: Native Language and Gender Distribution

| Native Language | ALS (F / M / Total) | HC (F / M / Total) | PD (F / M / Total) | Grand Total |
| :--- | :---: | :---: | :---: | :---: |
| **Assamese** | 1 / 0 / **1** | 1 / 2 / **3** | 0 / 2 / **2** | **6** |
| **Bengali** | 24 / 50 / **74** | 9 / 18 / **27** | 14 / 31 / **45** | **146** |
| **Bhojpuri** | 1 / 0 / **1** | 0 / 0 / **0** | 0 / 0 / **0** | **1** |
| **Chattisgarhi** | 0 / 0 / **0** | 0 / 1 / **1** | 0 / 0 / **0** | **1** |
| **English** | 0 / 1 / **1** | 1 / 0 / **1** | 0 / 0 / **0** | **2** |
| **Hindi** | 7 / 16 / **23** | 3 / 7 / **10** | 2 / 14 / **16** | **49** |
| **Kannada** | 9 / 23 / **32** | 48 / 84 / **132** | 9 / 31 / **40** | **204** |
| **Malayalam** | 5 / 8 / **13** | 1 / 2 / **3** | 3 / 6 / **9** | **25** |
| **Marathi** | 0 / 4 / **4** | 1 / 1 / **2** | 1 / 1 / **2** | **8** |
| **Odia** | 0 / 5 / **5** | 1 / 2 / **3** | 0 / 2 / **2** | **10** |
| **SSK** | 0 / 0 / **0** | 0 / 0 / **0** | 0 / 1 / **1** | **1** |
| **Tamil** | 5 / 12 / **17** | 5 / 5 / **10** | 7 / 15 / **22** | **49** |
| **Telugu** | 18 / 23 / **41** | 6 / 15 / **21** | 7 / 16 / **23** | **85** |
| **Tulu** | 0 / 0 / **0** | 0 / 2 / **2** | 0 / 0 / **0** | **2** |
| **Urdu** | 2 / 3 / **5** | 1 / 1 / **2** | 3 / 6 / **9** | **16** |
| **Grand Total** | **72 / 145 / 217** | **77 / 140 / 217** | **46 / 125 / 171** | **605** |

</details>

---

<details>
<summary><b>2. Browser Preview: Matched & Mismatched Evaluation (Data for Fig. 4)</b> (Click to expand)</summary>

<br>

> **Paper Reference:**  
> **Fig. 4.** *Mean 5-fold classification accuracy for ALS vs HC (left column) and PD vs HC (right column). In all six subplots, the x-axis represents the training task, while each row indicates the fixed test task (SPON, DIDK, or IMG). The ⋆ symbol marks Disease-specific matched-task evaluation. Raw wav, Source-only, Filter-only. Error bars denote std. dev.*  
>  
> 📊 **Source Excel File:** [`matched_&_mismatched_values.xlsx`](./matched_%26_mismatched_values.xlsx)

The tables below report **Mean F1 score (sd)** alongside **Mean Accuracy (sd)** across all acoustic representations and task combinations.

### 2.1. Fixed Test Task: SPON
| Condition | Representation | Trained on SPON ★ | Trained on DIDK | Trained on IMG |
| :--- | :--- | :---: | :---: | :---: |
| **ALS vs HC** | **Raw Wav** | F1: 0.9153 (0.0206)<br>Acc: 0.9103 (0.0229) | F1: 0.7955 (0.0130)<br>Acc: 0.7291 (0.0175) | F1: 0.9052 (0.0189)<br>Acc: 0.8978 (0.0216) |
| | **Source Only** | F1: 0.8666 (0.0336)<br>Acc: 0.8563 (0.0315) | F1: 0.7638 (0.0055)<br>Acc: 0.6794 (0.0208) | F1: 0.8403 (0.0342)<br>Acc: 0.8124 (0.0458) |
| | **Filter Only** | F1: 0.9132 (0.0157)<br>Acc: 0.9071 (0.0166) | F1: 0.7821 (0.0431)<br>Acc: 0.7080 (0.0676) | F1: 0.8408 (0.0301)<br>Acc: 0.8530 (0.0330) |
| **PD vs HC** | **Raw Wav** | F1: 0.9188 (0.0061)<br>Acc: 0.9065 (0.0056) | F1: 0.8821 (0.0158)<br>Acc: 0.8515 (0.0220) | F1: 0.9151 (0.0123)<br>Acc: 0.9024 (0.0128) |
| | **Source Only** | F1: 0.9011 (0.0207)<br>Acc: 0.8900 (0.0209) | F1: 0.7512 (0.0299)<br>Acc: 0.7679 (0.0246) | F1: 0.7512 (0.0299)<br>Acc: 0.7679 (0.0246) |
| | **Filter Only** | F1: 0.9173 (0.0041)<br>Acc: 0.9017 (0.0052) | F1: 0.8609 (0.0129)<br>Acc: 0.8222 (0.0198) | F1: 0.8609 (0.0129)<br>Acc: 0.8222 (0.0198) |

### 2.2. Fixed Test Task: DIDK
| Condition | Representation | Trained on SPON | Trained on DIDK ★ | Trained on IMG |
| :--- | :--- | :---: | :---: | :---: |
| **ALS vs HC** | **Raw Wav** | F1: 0.8780 (0.0102)<br>Acc: 0.8606 (0.0129) | F1: 0.9002 (0.0135)<br>Acc: 0.8877 (0.0188) | F1: 0.8785 (0.0137)<br>Acc: 0.8578 (0.0167) |
| | **Source Only** | F1: 0.7743 (0.0667)<br>Acc: 0.7614 (0.0519) | F1: 0.8318 (0.0270)<br>Acc: 0.8142 (0.0233) | F1: 0.7923 (0.0191)<br>Acc: 0.7598 (0.0193) |
| | **Filter Only** | F1: 0.8662 (0.0227)<br>Acc: 0.8492 (0.0288) | F1: 0.8792 (0.0294)<br>Acc: 0.8669 (0.0317) | F1: 0.8515 (0.0376)<br>Acc: 0.8524 (0.0367) |
| **PD vs HC** | **Raw Wav** | F1: 0.8043 (0.0197)<br>Acc: 0.7929 (0.0157) | F1: 0.8924 (0.0085)<br>Acc: 0.8734 (0.0075) | F1: 0.8485 (0.0208)<br>Acc: 0.8280 (0.0183) |
| | **Source Only** | F1: 0.7199 (0.0166)<br>Acc: 0.7209 (0.0182) | F1: 0.8032 (0.0157)<br>Acc: 0.7573 (0.0159) | F1: 0.8084 (0.0071)<br>Acc: 0.7637 (0.0071) |
| | **Filter Only** | F1: 0.8483 (0.0186)<br>Acc: 0.8237 (0.0164) | F1: 0.8588 (0.0160)<br>Acc: 0.8319 (0.0202) | F1: 0.8317 (0.0113)<br>Acc: 0.8071 (0.0090) |

### 2.3. Fixed Test Task: IMG
| Condition | Representation | Trained on SPON | Trained on DIDK | Trained on IMG ★ |
| :--- | :--- | :---: | :---: | :---: |
| **ALS vs HC** | **Raw Wav** | F1: 0.8351 (0.0182)<br>Acc: 0.8476 (0.0176) | F1: 0.7918 (0.0194)<br>Acc: 0.7562 (0.0255) | F1: 0.8653 (0.0177)<br>Acc: 0.8701 (0.0204) |
| | **Source Only** | F1: 0.7393 (0.0296)<br>Acc: 0.7345 (0.0192) | F1: 0.7219 (0.0205)<br>Acc: 0.6758 (0.0175) | F1: 0.7655 (0.0386)<br>Acc: 0.7742 (0.0403) |
| | **Filter Only** | F1: 0.8096 (0.0327)<br>Acc: 0.8250 (0.0325) | F1: 0.7504 (0.0296)<br>Acc: 0.7194 (0.0512) | F1: 0.8408 (0.0301)<br>Acc: 0.8530 (0.0330) |
| **PD vs HC** | **Raw Wav** | F1: 0.8367 (0.0272)<br>Acc: 0.8367 (0.0223) | F1: 0.8508 (0.0088)<br>Acc: 0.8275 (0.0113) | F1: 0.8836 (0.0182)<br>Acc: 0.8782 (0.0150) |
| | **Source Only** | F1: 0.7597 (0.0190)<br>Acc: 0.7602 (0.0184) | F1: 0.7499 (0.0191)<br>Acc: 0.7550 (0.0171) | F1: 0.8299 (0.0169)<br>Acc: 0.8272 (0.0119) |
| | **Filter Only** | F1: 0.8221 (0.0301)<br>Acc: 0.8153 (0.0205) | F1: 0.8073 (0.0085)<br>Acc: 0.7745 (0.0104) | F1: 0.8862 (0.0066)<br>Acc: 0.8758 (0.0053) |

</details>

---

<details>
<summary><b>3. Browser Preview: Disease-Specific vs. Cross-Disease Evaluation (Data for Fig. 5)</b> (Click to expand)</summary>

<br>

> **Paper Reference:**  
> **Fig. 5.** *Disease-specific matched-task and Cross-disease matched-task performance. Error bars denote std. dev. Left: testing on ALS vs HC. Right: testing on PD vs HC. Results are shown for SPON, DIDK, and IMG tasks using raw wav, source-only, and filter-only representations (mean 5-fold accuracy).*  
>  
> 📊 **Source Excel File:** [`cross_disease_values.xlsx`](./cross_disease_values.xlsx)

The tables below detail **Disease-Specific** vs **Cross-Disease** performance across each task, listing both **Mean F1 (sd)** and **Mean Acc (sd)**.

### 3.1. Evaluation on SPON
| Representation | Task Type | ALS vs HC Mean F1 (sd) | ALS vs HC Mean Acc (sd) | PD vs HC Mean F1 (sd) | PD vs HC Mean Acc (sd) |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Raw Wav** | Disease-Specific | 0.9153 (0.0206) | 0.9103 (0.0229) | 0.9188 (0.0061) | 0.9065 (0.0056) |
| | Cross-Disease | 0.9167 (0.0309) | 0.9155 (0.0284) | 0.9546 (0.0204) | 0.9508 (0.0213) |
| **Source Only** | Disease-Specific | 0.8666 (0.0336) | 0.8563 (0.0315) | 0.9011 (0.0207) | 0.8900 (0.0209) |
| | Cross-Disease | 0.8878 (0.0270) | 0.8878 (0.0272) | 0.8335 (0.0166) | 0.8238 (0.0160) |
| **Filter Only** | Disease-Specific | 0.9132 (0.0157) | 0.9071 (0.0166) | 0.9173 (0.0041) | 0.9017 (0.0052) |
| | Cross-Disease | 0.9281 (0.0162) | 0.9279 (0.0162) | 0.9145 (0.0244) | 0.9105 (0.0206) |

### 3.2. Evaluation on DIDK
| Representation | Task Type | ALS vs HC Mean F1 (sd) | ALS vs HC Mean Acc (sd) | PD vs HC Mean F1 (sd) | PD vs HC Mean Acc (sd) |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Raw Wav** | Disease-Specific | 0.9002 (0.0135) | 0.8877 (0.0188) | 0.8924 (0.0085) | 0.8734 (0.0075) |
| | Cross-Disease | 0.9168 (0.0128) | 0.9099 (0.0113) | 0.8553 (0.0165) | 0.8517 (0.0161) |
| **Source Only** | Disease-Specific | 0.8318 (0.0270) | 0.8142 (0.0233) | 0.8032 (0.0157) | 0.7573 (0.0159) |
| | Cross-Disease | 0.7638 (0.0040) | 0.7503 (0.0032) | 0.7729 (0.0342) | 0.7397 (0.0224) |
| **Filter Only** | Disease-Specific | 0.8792 (0.0294) | 0.8669 (0.0317) | 0.8588 (0.0160) | 0.8319 (0.0202) |
| | Cross-Disease | 0.7679 (0.0650) | 0.7722 (0.0586) | 0.8586 (0.0319) | 0.8586 (0.0319) |

### 3.3. Evaluation on IMG
| Representation | Task Type | ALS vs HC Mean F1 (sd) | ALS vs HC Mean Acc (sd) | PD vs HC Mean F1 (sd) | PD vs HC Mean Acc (sd) |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Raw Wav** | Disease-Specific | 0.8653 (0.0177) | 0.8701 (0.0204) | 0.8836 (0.0182) | 0.8782 (0.0150) |
| | Cross-Disease | 0.8887 (0.0248) | 0.8969 (0.0216) | 0.8793 (0.0295) | 0.8819 (0.0291) |
| **Source Only** | Disease-Specific | 0.7655 (0.0386) | 0.7742 (0.0403) | 0.8299 (0.0169) | 0.8272 (0.0119) |
| | Cross-Disease | 0.7707 (0.0389) | 0.7734 (0.0354) | 0.7671 (0.0312) | 0.7843 (0.0161) |
| **Filter Only** | Disease-Specific | 0.8408 (0.0301) | 0.8530 (0.0330) | 0.8862 (0.0066) | 0.8758 (0.0053) |
| | Cross-Disease | 0.8039 (0.0156) | 0.8073 (0.0153) | 0.8663 (0.0097) | 0.8728 (0.0105) |

</details>
