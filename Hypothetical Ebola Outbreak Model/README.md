# Hypothetical Ebola Outbreak Model
There are many files needed to run the simulations, they are:

* model-gamma.cka:     	  Main file, include the model
* observables.cka: 	      Here we define the variables (agents) of the system
* CL-4cities.cka:   	    Parameters of the country such as population, ratios between cities, link and transport


* To run the model, execute

`mpirun -np 4 path_to_piskas -i model-gamma.cka -i CL-4cities.cka -i observables.cka -p 100 -t 400 -sync-t 1`

where `-p 100` indicates the number of steps to save, `-t 400` the number of simulated days and `-sync-t 1` the synchronization time between compartments. In this case we are saving the result of the simulation once every four days.
