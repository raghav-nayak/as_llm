## Sharding
- Sharded models take significantly less memory compared to regular models.
- distributes computational workouts across different machines / devices
![[Pasted image 20240703144954.png]]

- useful with massive datasets which are too large to fit into the memory of a single machine


![[Pasted image 20240703145810.png]]


![[Pasted image 20240703145829.png]]

![[Pasted image 20240704123432.png]]


![[Pasted image 20240704123509.png]]

### 3 main steps in Sharding
##### 1. Model partitioning
- breaking down the model into manageable parts using
	- layers
	- neurons
	- data sets

##### 2. Distribution
- once the model is partitioned, each unit is assigned to different computational unit.
- these computational units can be
	- separate machine
	- processors
	- distributed nodes

##### 3. Parallel processing


#### aggregation
- After sharding, you need aggregation at the end.
- after processing, the results are aggregated(combined) to produce final output.

![[Pasted image 20240704124349.png]]

inference aggregation -> combining **predictions** from different parts of the model
training aggregation -> combining **radiance** 


Data parallel processing

Distributed data parallel processing
- distribute both data and processing across different devices
- speeds up the training and inference times

![[Pasted image 20240704124731.png]]

#### Fully Sharded Data Parallel(FSDP)
[article](https://engineering.fb.com/2021/07/15/open-source/fsdp/)
![[Pasted image 20240704124939.png]]
compared to other sharding techniques, FSDP shards the data uniformly.

[ZeRO: Memory Optimizations Toward Training Trillion Parameter Models research paper](https://arxiv.org/pdf/1910.02054)
- this uses Zero Redundancy Optimizer
- eliminating redundancies in data and leveraging model parallel trainings
- this does not have below given trade-offs or limitations
- focuses on model's state, not on data and parameters


other sharding techniques
- data parallelism
- pipeline parallelism
- model parallelism
- CPU offloading

these make trade-offs between
- functionality
- usability
- memory efficiency
- compute / communication efficiency

#### learning
sharding helps us to achieve same as quantization.
in real world scenarios, we combine sharding and quantization
