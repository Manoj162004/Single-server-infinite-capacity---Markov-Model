## Single server with infinite capacity (M/M/1):(oo/FIFO)
### Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

### Software required :
Visual components and Python

### Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

### Procedure :

![imAGE](2.png)
 
### Program
```
Developed by : Manoj S
Reg no : 212222100025
```
```
arr_tim=float(input("Enter the mean inter arrival time of the object From feeder(in sec):"))
ser_tim=float(input("Enter the mean inter service time of the Lathe machine(in sec):"))
Robot_tim=float(input("Enter the additional time taken for the robot (in sec):"))
lam=1/arr_tim
mu=1/(ser_tim+Robot_tim)
print("--------------------------------------")
print("Single Server with infinite Capacity -(M/M/1) :  (oo/FIFO)")
print("--------------------------------------")
print("The mean arrival rate per seconds %0.2f"%lam)
print("The mean service rate per seconds %0.2f"%mu)
if(lam < mu):
  Ns=lam/(mu-lam)
  Nq=Ns-(lam/mu)
  Ws=Ns/lam
  Wq=Nq/lam
  print("Average number of object in system : %0.2f "%Ns)
  print("Average number of objects in conveyor : %0.2f "%Nq)
  print("Average waiting time of an object in system : %0.2f sec"%Ws)
  print("Average waiting time of an object in conveyor : %0.2f sec"%Wq)
  print("Probability that the system is busy : %0.2f"%(lam/mu))
  print("Probability that the system is empty : %0.2f "%(1-(lam/mu)))
else :
  print("Warning ! Objects over flow will happen in the converyor ")
print("--------------------------------------") 
```
### Output :
![singleserveroo](https://github.com/Manoj162004/Single-server-infinite-capacity---Markov-Model/assets/120365042/5f1c48c2-235e-4738-a369-3119cf2e3afb)

### Result :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.

