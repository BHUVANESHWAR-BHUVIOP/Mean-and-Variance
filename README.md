#  Mean and variance of a discrete  distribution


## Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


## Software required :  

Python and Visual components tool

## Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


## Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


## Experiment :

![Input](IN1.png)
## Program :
NAME : BHUVANESHWAR V

REG NO : 212221240009
```
import numpy as np
L=[int(i) for i in input().split()]
N=len(L);
print(N)
M=max(L)
print(M)
x=list();frequency_of_x=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1
    frequency_of_x.append(c)
    x.append(i)
print(x)
print(frequency_of_x)
sum_of_frequency=np.sum(frequency_of_x)
print(sum_of_frequency)
prob_of_x=list()
for i in range(M+1):
    prob_of_x.append(frequency_of_x[i]/sum_of_frequency) 
mean=np.inner(x,prob_of_x)
print(mean)
EX2=np.inner(np.square(x),prob_of_x)
variance=EX2-mean**2 
print(variance)
standard_deviation=np.sqrt(variance)
print(standard_deviation)
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%variance) 
print("The Standard deviation of arrival from feeder is %.3F "%standard_deviation)

```
## Output : 
![Op](t1.png)
![Op](t2.png)
![Op](t3.png)
![Op](t4.png)
![Op](t5.png)
![Op](t6.png)

## Results :
To find mean and variance of arrival of objects from the feeder using probability distribution is successfully done and learnt
