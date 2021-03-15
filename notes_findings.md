# Notes and Findings

## Diabetic Retinopathy

- The original dataset is from a Kaggle competition. https://www.kaggle.com/c/diabetic-retinopathy-detection

- The file size is pretty massive (11GB)

- One of the participants resized the dataset https://www.kaggle.com/tanlikesmath/diabetic-retinopathy-resized

- This was downloaded for initial model creation.

- After download, a python script was used to divide them into individual folders for train and test

-  There is an imbalance in data labels

  - | DR severity | Number of images |
    | ----------: | ---------------- |
    |           0 | 25810            |
    |           1 | 2443             |
    |           2 | 5292             |
    |           3 | 873              |
    |           4 | 708              |

- Due to the imbalance in data labels, a stratified approach was used for train test split

- - | DR severity | Number of images (Training dataset) |
    | ----------: | ----------------------------------- |
    |           0 | 566                                 |
    |           1 | 567                                 |
    |           2 | 566                                 |
    |           3 | 566                                 |
    |           4 | 567                                 |

- We will eventually need more images. But having a repo of images from CHEERS is useful.
- 












## Glaucoma