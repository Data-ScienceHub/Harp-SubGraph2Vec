# Fascia in 1 CPU node

Link: https://github.com/francktcheng/fascia


## Hardware & Software

**One instance of AWS**



Instance Type: t2.micro

Model Name: Intel(R) Xeon(R) CPU E5-2676 v3 @ 2.40GHz

Operating System: Ubuntu 22.04.1 LTS

Count of vCPU: 1

Memory: 1G





## Results




### Graph500  Scale=20 - u3-1.fascia

*The format "mimo" cannot fit Fascia*

	
	

### Graph500  Scale=20 - u5-2.fascia

*The format "mimo" cannot fit Fascia*

	
	


### hpylo.graph   template.graph
<img width="695" alt="image" src="https://user-images.githubusercontent.com/41974269/215904122-7aeb9a65-f1ca-4f94-91c9-13fa5baf2a47.png">

```
Read in Data Time:
	 0.000216 seconds
Computation Time InnerParal Mode:
	 0.011630 seconds
Count:
	5.970082e+07
Total time:
	 0.012407 seconds
   
```




# Harp-SubGraph2Vec - MPI in Cluster of 2 CPU nodes


## Hardware & Software

**Two instances of AWS**



Instance Type: t2.micro

Model Name: Intel(R) Xeon(R) CPU E5-2676 v3 @ 2.40GHz

Operating System: Ubuntu 22.04.1 LTS

Count of vCPU: 1

Memory: 1G


## Results




### Graph500  Scale=20 - u3-1.fascia


<img width="441" alt="image" src="https://user-images.githubusercontent.com/41974269/215671923-408c3736-97dc-46a4-a6aa-418cba40a285.png">


```
Time for count per iter:  2.163445 seconds
spmv ratio 83.356406% 
eMA ratio 6.749021% 
Peak Mem Usage is :  0.345165 GB
SpMM time is : 0.680083 second; EMA time is: 0.145999 
SpMM Memory bandwidth is : 0.000000 GBytes per second
FMA Memory bandwidth is : 0.222462 GBytes per second
Total Memory bandwidth is : 0.039317 GBytes per second
SpMM Throughput is : 0.000000 Gflops per second
FMA Throughput is : 0.037077 Gflops per second
Total Throughput is : 0.006553 Gflops per second
Final raw count is 1.574638e+10
Prob is 0.222222
Final count is 7.085870e+10
```






### Graph500  Scale=20 - u5-2.fascia

<img width="440" alt="image" src="https://user-images.githubusercontent.com/41974269/215651259-41fe68a9-70d3-4130-9224-4ec4f469e42e.png">

```
Time for count per iter:  5.676107 seconds
spmv ratio 92.955208% 
eMA ratio 5.560924% 
Peak Mem Usage is :  0.463158 GB
SpMM time is : 3.179380 second; EMA time is: 0.315568 
SpMM Memory bandwidth is : 0.461492 GBytes per second
FMA Memory bandwidth is : 0.914870 GBytes per second
Total Memory bandwidth is : 0.502429 GBytes per second
SpMM Throughput is : 0.054293 Gflops per second
FMA Throughput is : 0.152478 Gflops per second
Total Throughput is : 0.063159 Gflops per second
Final raw count is 2.671182e+16
Prob is 0.038400
Final count is 6.956204e+17
```



# Harp-SubGraph2Vec in Single CPU node

## Hardware & Software

**One instance of AWS**



Instance Type: t2.micro

Model Name: Intel(R) Xeon(R) CPU E5-2676 v3 @ 2.40GHz

Operating System: Ubuntu 22.04.1 LTS

Count of vCPU: 1

Memory: 1G





## Results




### Graph500  Scale=20 - u3-1.fascia

*Out of Memory*

