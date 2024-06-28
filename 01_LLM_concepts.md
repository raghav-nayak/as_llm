#LLM

https://www.youtube.com/watch?v=ozKjpWZ-Z6w&list=PL5dTjWUk_cPZxyZuZdl8S0g4tbh-GL2Ro

**GPT** -> Generative Pre-Trainer Transformer
### Transformers
- transformers empower LLMs
- Something that transforms from one sequence to another
- input -> encoder                  decoder -> output
- sequence to sequence learning
- token means word
- encoder 
	- has multiple layers
	- a particular encoder layer generates encodings which
		- define which part of the input sequence are relevant to each other
		- passes these encodings to the next encoding layer
- decoder
	- takes all of the encodings and generates the output
- advantages
	- don't process data in an order
	- use "attention mechanism"
- transformers run multiple sequences in parallel to speed up training times
- use cases
	- translation
	- document summaries
	- creating own documents(blogs)
	- image processing like CNNs
- you don't "program" instructions, you "train" it
- need loads of "training" data
- training
	- e.g. bady
	- does not have usual manual
	- learns by observing 
	- pattern recognition
- require "back-propagation" where they undergo iterations to ensure the output is correct
- also required RLHF(reinforcement learning with human feedback)


![[Pasted image 20240628224934.png]]

Transformers -> Semi supervised learning -> Pre-trained in an unsupervised manner with a large data set -> Finetuned with supervised learning for better performance


### Recurrent neural networks(RNN) vs. Transformers
RNN
- RNNs work in order
- so they might not get an accurate result

Transformers
- will always be more accurate as focus on "context" and meaning and not the order
- this is "attention mechanism"


transformers -> LLMs / Gen AI -> Categories
- categories
	- Text to text
	- speech to text (e.g. Whisper)
	- text to speech
	- image to text
	- text to image (e.g. Dally, Midjourney)
	- text to audio(music)
	- text to video(e.g. Sora)


Multi modal 
- Text
- Docs
- Images
- Docs

Important terms
- matrices
- word embeddings
- back-propagation
