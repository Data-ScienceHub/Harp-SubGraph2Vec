# Harp-SubGraph2Vec

https://github.com/DSC-SPIDAL/harp/blob/cpuSC/README.md
https://github.com/DSC-SPIDAL/harp/blob/gpuSC/README.md




# The experiments for the followings and attached the results;

Single node and MPI:
Miami u12-2.fascia
Miami u13.fascia
Orkut u12-2.fascia
Orkut u13.fascia

GPU:
Miami u7-1.fascia
Miami u10-1.fascia
Orkut u7-1.fascia
Orkut u10-1.fascia
(Due to segmentation error I had to reduce template size)



# Just verified these:

CPU with MPI. Tested on two nodes j-001, j-002 on Juliet.

mpirun -f mpihosts.txt -n 4 -ppn 1 -genv OMP_NUM_THREADS=24 -genv I_MPI_PIN_DOMAIN=omp sc-hsw-icc-mpiicc.bin /share/project/FG474/TrainingData/subgraph/Edge-Graph/miami.graph /share/project/FG474/TrainingData/subgraph/template/u10-1.fascia 1 24 0 0 1 1 1


GPU:

./sc-gpu-gnu.bin /share/project/FG474/TrainingData/subgraph/Edge-Graph/miami.graph /share/project/FG474/TrainingData/subgraph/template/u10-1.fascia 1 24 0 0 1 1


VE with MPI:

OMP_NUM_THREADS=8; mpirun -ve 0-3 -np 4 sc-nec-ncc.bin /share/project/FG474/TrainingData/subgraph/CSC-binary/miami.csc.data /share/project/FG474/TrainingData/subgraph/template/u10-1.fascia 1 8 1 0 1 1

# Make sure that you set up the path correct. e.g.
 set the path to the u13.fascia file? The templates are in /share/project/FG474/TrainingData/subgraph/template/.
