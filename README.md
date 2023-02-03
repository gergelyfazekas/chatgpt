# Chat GPT
## Code refactoring using OpenAI's ChatGPT with the text-davinci-003 engine

This module is focused on helping us write faster, more coherent and more pythonic code. We can ask OpenAI's ChatGPT model to make suggestions about our own code. The suggestions themselves can be in the form of english text or directly python code (in which case the model changes/refactors our code per its suggestion).

The two main methods to interact with the NLP model are suggest() and create_conversation(). These are instance methods of the ChatGPT class.
Both methods return suggestions, explanations or answers for a specific user-written function that is either defined in the same environment or imported. The suggestions can be focused on 3 topics at the moment: increasing speed, altering code style or explaining what the function does. 

### Example usage:

<img width="1138" alt="Screenshot 2023-02-02 at 16 49 20" src="https://user-images.githubusercontent.com/93786486/216373017-879c036a-e3c0-4416-bad5-1dfb225245b5.png">

We can call the suggest method on our ChatGPT instance. We can specify the focus and if code should be returned 
(and other kwargs modifying the response's length or randomness).

<img width="1213" alt="Screenshot 2023-02-03 at 16 23 18" src="https://user-images.githubusercontent.com/93786486/216640778-c150125c-ae9e-4583-ba69-4450a8eea824.png">


We can continue the conversation if we are not satisfied with the answer by calling create_conversation with the parameters shown below. 
To continue the conversation we have to set the forget parameter to False (so that the memory is not emptied) and we can specify a remind_me parameter to be able to look at what's in the model memory (our conversation so far, including the function we inspected and the suggestions it made for us).
We can either specify the next question as an argument or wait for the input prompt.
We can exit from the create_conversation function by typing "BYE" or "QUIT".

<img width="1213" alt="Screenshot 2023-02-03 at 16 23 38" src="https://user-images.githubusercontent.com/93786486/216640863-7c3f28a4-3937-42ef-b66e-1a1d8b9c4c23.png">

