Finetuning

![[Pasted image 20240707133534.png]]


![[Pasted image 20240707133600.png]]

![[Pasted image 20240707133640.png]]


![[Pasted image 20240707133705.png]]


Finetuning
- taking one pre-trained model and training at least one of the parameters of the model with some data

![[Pasted image 20240707133852.png]]


![[Pasted image 20240707133924.png]]


![[Pasted image 20240707134022.png]]

![[Pasted image 20240707134053.png]]

![[Pasted image 20240707134118.png]]

![[Pasted image 20240707134142.png]]

smaller models, which are finetuned, can outperform the large models.
![[Pasted image 20240707134200.png]]

![[Pasted image 20240707134325.png]]

![[Pasted image 20240707134349.png]]


difference between Training and Finetunig
- in finetuning, the data we provide is specific to our usecase or narrow usecase
![[Pasted image 20240707134403.png]]


supervised learning
- we have the input and expected output, and we tell the model how to think and act.
![[Pasted image 20240707134522.png]]



#### Reinforcement Learning
![[Pasted image 20240707134823.png]]

3 stages of reinforcement learning
- supervised learning
- training a reward model
- reinforcement learning with PPO algorithm



#### finetuning process

![[Pasted image 20240707135112.png]]

![[Pasted image 20240707135524.png]]

![[Pasted image 20240707135924.png]]
1. Select dataset (based on factors)
	- Select version and format (have the right data) / 
	- Curation (curate relevant data after cleaning and massaging) / 
	- Synthetic data generation (use synthetic data generation for niche use case)
2. Task formulation
3. Model architecture and parameter adjustment
4. Finetuning process
	- Initialization
	- Training
		- backprogagation
		- gradient descent
	- Validation
	- HyperParameter Finetuning
		- learning rate
		- batch size
		- regularization strength
5. Evaluation
6. Deploy the model
7. Integrate into other systems and applications
