# MLforChem
## Machine learning models for ground state energy predictions
There are copious amounts of molecules whose ground state energies would have to be calculated to determine appropriate use in applications (i.e drug discovery). Possibly years of calculations would be needed to obtain the energies of all molecules.
A machine learning model can be trained to predict the ground state of a given molecule. In this project multiple models are tested to determine which model is able to predict the energies better.
## Data
The dataset was obtained from Kaggle. However the group who made the data available obtained the structure of the molecules from PubChem. The data consists of 16242 molecules each containing atoms C, H, O, N, P, S. and each molecule consists of 50 atoms or less.
The features are flattened entries of the upper triangular part of the Coulomb matrix. The dimension of  the entire dataset is 16242 by 1275.
## Results
The ambiguous representation of molecules by the Coulomb matrix was addressed by using the eigenvalues of the matrix as features. The errors achieved are considerably small and predictions are off by about 0.151 Rydberg in average (approximately 0.25 Kcal/mol)
Using this reduced dataset resulted in models prediction errors to increase by 2% but the training time decrease significantly, 90%, when using the eigenvalues.
The XGboost regressor model performed the best. Furthermore, training this model took less time than the random forest and the neural network models.
