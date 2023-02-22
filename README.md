# ChatGPT-Q-A-Chatbot-with-custom-data
ChatGPT chatbots with customised knowledge. Train ChatGPT on a niche set of knowledge that ChatGPT does not know about. Written in Python so, of course install python if you don't have it.

How to use
==========
Step 1 - pip install gpt_index

Step 2 - pip install langchain

Step 3 - edit key_openai.txt and put your own api key there. Register an account at openai.com if you don't have one.

Step 4 - Try asking chat gpt via the normal chat gpt interface "what does sex 1.0 mean" or any of the other questions contained in /data/training.txt and you will see that it does not know. This info is contained in a book I wrote called Sex 3.0 which you can find here on amazon https://www.amazon.com/Sex-3-0-Sexual-Revolution-Manual/dp/1468134329 but GPT has never read it

Step 5 - From the command line use 'python chatbot.py' to run the training and the bot and ask it about sex 1.0, 2.0 or 3.0. Their core designs and the eras that they exist in and it can now answer all the questions contained in /data/training.txt so just put the info your want to train gpt with in this file instead.

Step 6 - If you quit the program and then comment out line 44. The line that trains GPT that goes "index = construct_index("data/")" and run the program again and ask the same questions you will see that it has retained the new training without needing to be trained again as it is based off your API key.
