### Post Training Quantization(PTQ)
- after model is trained, we can apply PTQ

![[Pasted image 20240701220454.png]]

PTQ process
- Weight Quantization
	- Higher Precision(32 bit) -> +-3.4x10<sup>38</sup>
	- Lower precision(8 bit) -> -128 to 127
- Activation Quantization
	- activations -> outputs generated by the neurons or nodes in each layer of the network
- Determining Quantization Range
	- this range is determined by calibration techniques.
	- Static calibration
		- Happens offline and **pre-inference**
	- Dynamic calibration
		- Happens **during inference** 
		- more accurate needs more computation


##### Symmetric Quantization
![[Pasted image 20240702110433.png]]

##### Asymmetric quantization
![[Pasted image 20240702110543.png]]



##### Per-channel quantization
- better precision
- each channel of a tensor is quantized independently
- tensor here means output channels of a convolutional layer

##### Per-tensor quantization
- more efficient
- the entire tensor is quantized as a single entity
- tensor here means weights or activations
- the quantization parameters are calculated for the entire tensor, considering all elements collectively

Two important libraries
1. TensorFlow Model Optimization Toolkit
2. Nvidia's TensorRT Open Source Software


#### Quantization Techniques

![[Pasted image 20240702111241.png]]


##### GPT Q
- post-training quantization method for 4-bit quantization
- focused on **GPU** inference and performance
- to compress a weights to a 4-bit quantization by minimizing the mean squared error that weight
- during inference, it will dynamically dequantize its weights to float16 for improved performance whilst keeping memory low
- disadvantage -> requires hardware to run it

##### GGUF
- Previously known as GGML
- allows users to use the **CPU** to run an LLLM 
- **Offload** some of its layers to the GPU for a speed up
- incredible format for those running models on CPU or Apple devices
- useful for smaller models and more capable models e.g. Mistral 7B 

AWQ
- Activation-aware Weight Quantization(AWQ)
- similar to GPTQ
- Unlike GPTQ, not all weights are equally important for an LLM's performance, which results in quantization loss
- skip weights during quantization
- a significant speed-up compared to GPTQ whilst keeping similar, or sometimes even better, performance

check TheBloke on HuggingFace -> for pre-quantized models
