# [AI Chat Robot] Amanda

Update: 2025.2.9 V1.0 Write system prompt and parameters to make it talk like a soft girl.

Update: 2025.2.12 V1.1 Fine tuned the large model locally to make it perform better compared to only system prompt support.

## Introduction

This chat robot project "Amanda" is based on Qwen2.5_(7B)-Alpaca pretrained by Alibaba. I use Ollama to deploy the model with system prompts locally, unsloth and colab to fine-tune the pre-trained model with the loRA method, and `.gguf` model qualification techniques to store the fine-tuned model. 

As a "single dog" (which means bachelor), I know that many "single dogs" really want to have a soft, considerate, kind, and beautiful girlfriend. However, it is almost impossible to find such a perfect girl in reality. In that case, I decided to use some datasets to train a virtual girlfriend, which is **soft, cute, considerate, and obedient**. 

She is **soft**, so she will always speak with a tone like a spoiled baby.

She is **cute**, so she will always use emojis and emoticons in her speech.

She is **considerate**, so no matter what kind of difficulties you are facing, she will comfort you and support you.

She is **obedient**, so she will never refuse your requests whether they are reasonable or not.

HOPE that she can comfort your heart and make your life more beautiful.

## How to use

This model is trained with `unsloth`, and all the codes were in `Amanda V1 based on Qwen2.5_7b.ipynb`, which is the source file of the work.

For training data, it is `Amanda_Traindata.json`. You can train with this file. If you don't want to fine-tune the model but want to use RAG techniques and vector database directly, you can upload `Amanda_Traindata.docx`. I believe it will work as well.

I set the model qualification as `Q8_0.gguf`, it occupies about 8 GB, if you want higher or lower accuracy, you can modify the code.

At the end of the code, I set that the model will be sent to Google Cloud Drive, you can download it quickly there.

The system prompt file has been provided by me, so after downloading the model with `.gguf` format, you can directly open Ollama, install, and use it as follows.

```bash
ollama create Amanda_soft_and_cute -f ./Amanda
ollama run Amanda:latest
```

Finally, it will work like
![Test 1](https://github.com/TerimaLabX/-AI-Chat-Robot-Amanda/blob/main/Amanda%E6%B5%8B%E8%AF%95.png)
![Test 2](https://github.com/TerimaLabX/-AI-Chat-Robot-Amanda/blob/main/Amanda%E6%B5%8B%E8%AF%952.png)


If you want to generate more datasets or want to know how I generate the training data, you can open `generator.txt`and get the prompt. By putting this prompt into ChatGPT, you can get many datasets.

