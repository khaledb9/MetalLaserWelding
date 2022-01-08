# MetalLaserWelding

Codes used in "A multiscale approach for modeling metal laser welding" https://doi.org/10.1063/5.0043764

- The idea of this code is to model metal laser welding considering the fast heating rates of electrons and correct the models performing the welding purely  on the MD lattice, skipping the high thermal conductivity and low heat capacity of electrons in metals.

- The proposed scheme allows the proper description of heat transfer in metals during laser welding and gives insights into the structure evolution of the lattice during the process. Please refer to the paper for detailed explanations.  

- You need to have a data file that is relaxed at some temperature (here at 300K). I provided a relaxation code for fast reproduction of the results. 

- This model can be used with CPU only. However, I found that using GPU gives you 5 times the computation speed ! I do understand that some potentials cannot use GPU. It is simple to remove the gpu setup in the code and it does not interfere with the dynamics of the simulation.

- Note that you MUST use the provided function.cpp and function.h and rebuild lammps because they contain the function that represents the 3D laser beam described in the paper. 

- Enough details are provided in the comments of the code. Feel free to contact me regarding any questions!
