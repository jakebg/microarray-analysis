
# Microarray data analysis on Leukemia cells

## ALL vs AML
ALL (Acute lymphoblastic leukemia) - a fast-growing form of cancer of the blood and bone marrow

AML (Acute myeloid leukemia) - typically slow-growing cancer that begins in lymphocytes in the bone marrow and extends into the blood

## Methods
1. Preprocess (Using pandas, and csv packages)
2. Feature selection using training data set
  a. Ttest, top 50 genes, smallest p-values
3. kNN classifier
  a. Choose distance algorithms
  
## Results
- Euclidian, k=3 accuracy of predicted training values 97.4%
                                     testing values  91.4%
- Euclidian, k=5                       training values 97.4%
                                     testing values  91.4%
- Manhattan, k=3                       training values 97.4%
                                     testing values  97.1%
- Manhattan, k=5                       training values 100%
                                     testing values  94.3%
- Jury Decision, k=3                   training values 97.4%
                                     testing values  100%
- Jury Decision, k=5                   training values 97.4%
                                     testing values  100%
                                     
- Leukemia Vector:             [0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 1 1 1 1]  35/35
- Euclidian, k=3 prediction:   [0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 0 1 1 1 0 1 0 1 1 1]  32/35
- Euclidian, k=5 prediction:   [0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 0 0 1 1 1 1 0 1 1 1]  32/35
- Manhattan, k=3 prediction:   [0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 0 1 1 1 1 1 1 1 1 1]  34/35
- Manhattan, k=5 prediction:   [0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 0 1 1 1 1 1 0 1 1 1]  33/35

## Conclusion
* Leukemia is a cancer that starts in the bone marrow, classified as ALL or AML 
* We successfully wrote a program to input a large data set, trim insignificant data, and predict ALL or AML classification in genes
* Our program uses a K-Nearest Neighbor (KNN) classifier, which predicts an output based on the nearest neighbors to the input
* We trained our KNN classifier with a base training set, and used 3 different distance measurement formulas to predict Leukemia classification
* Our most accurate prediction was using the Manhattan distance formula with the 3 nearest neighbors, resulting in 97.14% accuracy


