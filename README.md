# T5-Transformers-for-Indian-News-Summary

T5 stands for “Text-to-Text Transfer Transformer”. T5 introduced the “Text-to-Text” framework, in which every NLP task (Translation, Classification, question answering, etc.) has the same underlying structure in which text is fed as input to the model and text is produced as output. This means we can use the same model, same hyperparameters, and same loss function across all the tasks.

To understand that, we need to first understand two unique features of the T5 model:

Input/output Representation: Text-to-Text Framework
Training dataset: C4 dataset
This is done by adding a task-specific prefix to the input sequence and pre-training the model to get prefix-specific outputs.
In this case for summarizing we need to add the “summarize:” prefix to the input sequence.

T5 was trained on the C4 (Colossal Clean Crawled Corpus) dataset. The authors, through experimentation, came to the conclusion that the best performance is provided when the model is trained for 1 million steps with a batch size of 2 power 11 sequences of 512 lengths.

inshorts is a news app that summarizes long news articles in 60 words. The following dataset used contains the same: https://github.com/theachalshah/T5-Transformers-for-Indian-News-Summary/blob/main/news_summary.csv


Evaluation:-

Loss on last epoch = 0.73

Actual Summary – PM Narendra Modi on Thursday launched Ude Desh ka Aam Nagrik (UDAN) scheme for regional flight connectivity by flagging off the inaugural flight from Shimla to Delhi. Under UDAN, government will connect small towns by air with 50% plane seats’ fare

Predicted Summary – the first UDAN flight took off from Shimla on Wednesday after being flagged by PM Narendra Modi. The scheme, which seeks to make flying more affordable for common people, has been described as “a first-of its kind globally”. Under UDA, 50% of seats on each flight would have capped at?2,500 per seat/hour. It will be operated under Alliance Air’ regional arm of Air India. This comes after Prime Minister Narendra Modiji handed over boarding passes to some passengers travelling via the first launch flights starting from Shilkhand today.
