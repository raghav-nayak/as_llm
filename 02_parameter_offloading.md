Different LLMs
- Dolphin -> 3B
- Mistral -> 7B
- LLaMa -> 70B
- Falcon -> 180B
- ChatGPT 4 -> 1.7T

To run a model you need multiple high end GPUs

Quantization
- to run on a more affordable hardware, we need to compress large model into smaller one

![[Pasted image 20240629225109.png]]

we can offload the LLM parameters to a cheaper storage like RAM or SSDs 

*check about "fast inference of mixture-of-experts language models with offloading"*

inference -> LLM running to produce a result


Mixture of experts block

Mixtral 8X7B (mixture of 8 LLMs)


**Parameter offloading**
process
	- Divided into
		- essential parameters
			- required for every inference operation
			- kept in the main memory of the device
		- non-essential parameters
			- less frequently accessed
				- can be identified based on their access patterns during inference
					- The non-essential parameters identified for offloading and stored in external storage such as solid-state drives(SSDs), hard disk drives(HHDs), or cloud storage
				- parameters that are rarely accessed or are only need for specific parts of the models architecture can be candidates for offloading
			- can be offloaded to external storage
				- when non-essential parameters are required for a specific operation or layer of the models, they are loaded from external storage into the main memory on-demand
	- During **inference**, only the essential parameters are loaded into the main memory of the device
	- To minimize latency and improve performance, parameter offloading systems often use caching and prefetching techniques
	- Caches copies of frequently accessed non-essential parameters may be kept in memory to reduce the need for repeated loading from external storage
	- **Prefetching** involves proactively loading non-essential parameters into memory ahead of time based on predictions or heuristics about future access patterns
	- Some parameters offloading systems may employ **adaptive strategies** to dynamically adjust the set of parameters that are offloaded based on the available resources and workload characteristics.
	- e.g. parameters may be offloaded or loaded back into memory based on memory constraints, processing demands, or the frequency of parameter access during inference
	- To further reduce storage requirements and access latency, parameter offloading systems may employ **compression and optimization** techniques
	- parameters may be compressed using algorithms such as **quantization**, pruning, or **low-rank factorization** to reduce their size without significantly impacting model performance
	- Parameter offloading techniques can be integrated with specialized hardware accelerators such as GPUs, TPUs, or ASICs to improve performance and efficiency
	- Hardware accelerators can accelerate the loading and processing of parameters, reducing inference latency and energy consumption.
