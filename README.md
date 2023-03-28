# ChatGPT-Q-A-Chatbot-with-custom-data
ChatGPT chatbots with customised knowledge. Train ChatGPT on a niche set of knowledge that ChatGPT does not know about. Written in Python so, of course install python if you don't have it.

How to use
==========
Step 1 - pip install gpt_index

Step 2 - pip install langchain

Step 3 - edit key_openai.txt and put your own api key there. Register an account at openai.com if you don't have one.

Step 4 - Try asking chat gpt via the normal chat gpt interface "what does sex 1.0 mean" or any of the other questions contained in /data/training.txt and you will see that it does not know. This info is contained in a book I wrote called Sex 3.0 which is about a cognitive model of how to relate in the romantic / sexual realm. You can find here on amazon https://www.amazon.com/Sex-3-0-Sexual-Revolution-Manual/dp/1468134329 but GPT has never read it

Step 5 - From the command line use 'python chatbot.py' to run the training and the bot and ask it about sex 1.0, 2.0 or 3.0. Their core designs and the eras that they exist in and it can now answer all the questions contained in /data/training.txt so just put the info your want to train gpt with in this file instead.

Step 6 - If you quit the program and then comment out line 44. The line that trains GPT that goes "index = construct_index("data/")" and run the program again and ask the same questions you will see that it has retained the new training without needing to be trained again as it is based off the training data in the .json file that you already created.

Step 7 (optional) - If you want to enable PDF support you only need to add one line to this code. Just add 'import PyPDF2' at the top with the rest of the import statements (of couse you need to 'pip install PyPDF2' for this to work). As this code uses SimpleDirectoryReader that means that it will read every .txt and, if you add import PyPDF2, every PDF in the /data folder. It will vectorise all of them in order to create your .json file. So if you don't want old training data to be added into your .json file when it is being created then move it out of the /data dir and put it somewhere else. Only files that you want to be part of your .json file should be in the data folder.
