# Gene Regulatory Network Models

* To simulate using KaSim v3.5 (not the master branch):

`path_to_kasim -i model.ka -t 1000 -p 1000 -o model.out.txt -batch`

* To simulate using PISKaS v1.3, the model should be modified with the following statements in the top of the file:

`%compartment: cell 1`

`%use: cell`

then

`mpirun -np 1 path_to_piskas -i model.cka -t 1000 -p 1000 -o model. -sync-t 1`

* For the combined model between the Core Gene Regulatory Network and the Plasmid Replication, please execute the following

`mpirun -np 2 path_to_piskas -i combined_model.cka -t 1000 -p 1000 -o model. -sync-t 1`
