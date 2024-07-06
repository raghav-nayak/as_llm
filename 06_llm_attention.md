[Attention paper](https://arxiv.org/abs/1706.03762)
must read paper 
![[Pasted image 20240706130347.png]]

![[Pasted image 20240706130534.png]]

To understand attention, we need to understand embeddings.

Embedding
- how LLMs represent info
- bridge between humans and computers
- better the embedding == hight quality LLM == better the words are represented

![[Pasted image 20240706131327.png]]

e.g.
adding python to the embeddings
![[Pasted image 20240706131505.png]]


Two types of attentions
- self attention
	- **uses context** of a sentence and other words in the sentence **to resolve the ambiguity**
- multi-head attention
	- uses multiple embeddings of a model with  different variations
	- it uses transform operations
	![[Pasted image 20240706135956.png]]
- it has some summation functions and linear transformations
	![[Pasted image 20240706140031.png]]
