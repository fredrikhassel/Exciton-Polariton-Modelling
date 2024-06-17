# Exciton-Polariton-Modelling - Fredrik Hasselgren
Codebase for BSc project on modelling the strong coupling of excitons to cavity photons in curpous oxide.

The project was completed at the University of St Andrews, alongside the Microcavities group, lead by Dr. Hamid Ohadi. [https://ohadi.group/]

The experimental data used for the project was provided by the group, and associated with their paper: https://www.nature.com/articles/s41563-022-01230-4.

A detailed explanation of the project is available in the project report.

## Code

### Data extraction and analysis
The first part of the code is the most specific to the experimental data used, and so the least transferrable. The code determines the location, linewidth, and associated area of excitonic peaks present in a dataset of absorption coefficients of Cu2O.

The code perfoms a curve fit of the whole absorption data to determine values regarding the 11 excitonic peaks present, alongside three phonon backgrounds, and an initial offset. These values are used in the model.

### Coupled oscillator model

Exciton-polaritons are modelled using a coupled oscillator model, based on a 2 x 2 script created by Dr. Ohadi. The model incorporates 11 excitons coupled to a cavity photon but not each other. Eigenenergies of this configuration are determined, alonside hopfield coefficients indicating the relative presence of the polariton modes. Ultimately, the eigenvalues and eigenvectors of the 12 x 12 hamiltonian associated with the system is used to determine the polariton intensity as a function of energy and momentum.

### Transfer Matrix Method

Also in the code is a transfer matrix method representation of the optical setup used, based on code created by Dr. Sai Rajendran. This method allows us to determine the cavity linewidth, as well as its dependence on the energy of light used. These results are then incroporated into the coupled oscillator model.

### Code availability

The full project code is available, with the file titled "Cleaned main" containing the main code with extra comments and annotations.

### Citations
All resources consulted in the development of the present codebase is extensively cited in the project report.
