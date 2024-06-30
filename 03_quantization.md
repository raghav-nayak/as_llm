#LLM 

LLMs are really good at
- natural language processing(NLP)
	- translation
	- text summarization
	- text generation

Challenges
- Deploying LLMs if you don't have humungous GPUs


LLM works by representing words as numbers.
For accuracy, LLMs use high precision floating point number.
So, for high precision number needs a large GPU. 
If you reduce the precision(fixed point numbers or integers), it needs a small GPU.


![[Pasted image 20240630115340.png]]

While inference(processing prompt), LLM needs a large GPU with significant computational resources. This makes to run them on resource constraint devices.

#### Pre-Quantization
- converting parameters into lower precision before deployment.

Steps:
### 1. Identification of parameters that can be quantized

this will lead to accuracy degradation. So, we need to balance between
- performance
- precision

##### Quantization Aware Training
- Model will be quantized in the future, so train accordingly.
- so there by optimizing performance or precision



### 2. Select the right quantization scheme
a. fixed point
	8bit - 4bit for int + 4bit for fractional
	predicted
b. dynamic fixed point
	mix of floating point and fix point
	based on distribution of data, the precision can be adjusted dynamically
c. mixed precision
	we take decision based on the input 
	i.e. importance or sensitivity


### 3. Quantization process
a. Scaling
b. rounding
c. clipping
d. storage

### 4. Validation and fine tuning
