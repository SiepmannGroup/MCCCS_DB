# Alkanediol-Solvent Desorption Dataset

Canonical (*N*<sub>1</sub>*N*<sub>2</sub>*VT*) Gibbs ensemble Monte Carlo simulations were performed to model a single-stage equilibrium desorption process for (1,4-butanediol or 1,5-pentanediol)/water and 1,5-pentanediol/ethanol from all-silica MFI zeolite and 1,5-pentanediol/water from all-silica LTA zeolite. The equilibrium loadings in the zeolite phase were measured as a function of initial loading (*N*<sub>1</sub>, *N*<sub>2</sub>), vapor phase volume (*V*) and temperature (*T*).

### Format
This dataset is provided as tables. Each table contains the desorption equilibrium loading data for one zeolite-sorbate system. One entry (row) in the table includes 6 values, which are:
 * Total numbers of 2 molecules in the whole system (also initial loadings)
 * Volume of the vapor simulation box in Å<sup>3</sup>
 * Temperature in K, and 
 * 2 equilibrium loadings.

Initial and equilibrium loadings are provided as numbers of molecules. All extensive quantities except vapor volumes are normalized by the total amount of 
unit cells used in the simulation (12 for MFI, 27 for LTA) so that they correspond to 1 unit cell of the zeolite.  1024 state points (*N*<sub>1</sub>*N*<sub>2</sub>*VT* combinations) were measured by 32 independent simulations at each state point.

### Files
Below are the files containing tables for this dataset. The prefix (e.g., MFI-C5-W) indicates the zeolite, alkanediol and solvent for the simulation system. 
C4: 1,4-butanediol; C5: 1,5-butanediol; W: water; E: ethanol. The suffix <code>-all</code> includes the results for all independent simulations, giving a 32768x6 table for each file. 
The suffix <code>-stat</code> represents the independent simulations as means and standard deviations, giving a 1024x8 table for each file. All tables are stored in the CSV format.


```
MFI-C5-W-all.csv	MFI-C5-W-stat.csv
MFI-C4-W-all.csv	MFI-C4-W-stat.csv
MFI-C5-E-all.csv	MFI-C5-E-stat.csv
LTA-C5-W-all.csv	LTA-C5-W-stat.csv
```
Also, tabular simulation data for unary sorption of the components involved above are provided in the ```unary/``` directory for users who wish to apply prediction models requiring unary sorption data (ideal adsorbed solution theory, for example). The naming and column format are the same as the main dataset, while there are one initial and one equilibrium loading in each file.


### Source
This dataset is generated from molecular simulations as described in this manuscript: 
* Y. Sun, R. F. DeJaco, J. I. Siepmann, Deep Neural Network Learning of Complex Binary Sorption Equilibria from Molecular Simulation Data, *Chem. Sci.* **2019**, DOI: 10.1039/C8SC05340E 
See the supporting information for simulation details.
