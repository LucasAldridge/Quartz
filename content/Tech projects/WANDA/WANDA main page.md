This will serve as the primary information page about WANDA as a whole. If you just wanna learn about MY program, this is where you'd do that. But, if you wanna learn about the individual PARTS of my program, that will be in other documents found in the same folder.

# What is WANDA?
___
WANDA is an open-source AI assistant I wrote from scratch designed to work like Alexa or Siri, just FULLY AI. Basically, you get to yell at a box across the room and talk to ChatGPT. It costs literal pennies unless you're absolutely spamming requests, and should be able to do just about whatever ChatGPT can do, minus the visual stuff.

# How does it work?
___
WANDA uses OpenAI and 11Labs' APIs to generate and audibly speak to you in real time. The process looks like this...

- WANDA starts up
- WANDA listens and stores NO data of what it hears
- When the wakeup keyword is spoken, WANDA wakes up and waits for a question
- WANDA listens to the question and feeds it into GPT-4 mini 
- GPT-4 response is streamed directly into 11Labs' text to speech AI
- 11Labs' text to speech AI response is played through MPV in subprocess. 
- While playing the response, WANDA listens for a stop keyword, and if heard, stops speaking the response. 
# What features does WANDA include?
___
Currently, WANDA can only provide responses based on training data or can search the internet. However, many features are planned and will be coming at a variety of degrees of soon-ness

# What features are planned?
___
- Specific Date and Time functions
- Specific weather functions
- File read/write specific to your use-case (EX: could save recipes it comes up with for later reference)
- Playing local music files
- WLED integration

