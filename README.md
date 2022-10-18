# text-augmentation-translator
In this exercise, we are trying to augment new text data by translating the original data to other languages, and back-translate it to its original language.

Problem statement: We don't have much data to train our model. Therefore, we want to create/augment more data to improve the learning curve of our model and, ultimately, produce a better prediction. 

Objective: Create/augment text data by translating said text to other languages, and back-translate it to it's original language.

Solutions: We are trying out two methods, mBERT and DeepL API. mBERT is a state of the art model from the transformers library (Hugging Face), developed by Facebook, while DeepL is an API developed by a company of the same name. There are pros and cons with either approach, and in this exercise, we will explore some of the most important differentiators between the two approaches.

mBERT is a free library that allows you to translate any amount of text that you want, as long as your hardware allows it. On the other hand, DeepL is an API that offers a free usage to translate text up to 500,000 characters. Based on this comparison alone, mBERT seems to be a better option. However, mBERT model is taxing on your memory usage. It will limit the number of tokens that you can input to the model, in which if you are using Google Colab, you will have to set your max_length to 400. You will also need to batch the data to be able to input the text into the model. Moreover, working with mBERT is pretty complex and is not beginner friendly. You can check the starter code to translate your text data on this [Google Colab notebook](https://colab.research.google.com/drive/1YOcADEerK4a05HHML6fSIZ8xnqiTH91g#scrollTo=lweu9qYR5Xf7).

DeepL ,the other hand, is really easy to use and allows you translate every bit of your text regardless of your hardware capability. The API runtime is also pretty quick relative to mBERT. The only downside to this API is that, as a free user, you can only translate 500,000 characters (CHARACTERS, not words or tokens) per month. You can check the starter code to translate your text data on this [Google Colab notebook](https://colab.research.google.com/drive/1wx_JQ3Hj41voCxrz9wWIAU6Ba8k2JpjY#scrollTo=6azaKPygish4).
