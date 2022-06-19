# youtube-comment-analysis

A study of the hateful comments of YouTube comments. The proof of concept of this application is conducted on different sections of news including entertainment, world news, business news, sports, and science & technology. 

Process: 
1. The model was trained on raw (social media) text (tweets) to classify between 2 classes: hate_speech and not_hate_speech. We used BERT Base. There were other flavours of BERT that could have been used, such as BERTweet, DistilBERT and RoBERTa) and adapted it to our classification problem. 
2. The pre-trained model is a BERT Base, which is later adapted to our specific classification problem. The two datasets utilized for the training are: 
  - T-davidson_hate-speech-and-offensive-language: https://github.com/t-davidson/hate-speech-and-offensive-language/tree/master/data
  - Ucberkeley-dlab_measuring-hate-speech: https://huggingface.co/datasets/ucberkeley-dlab/measuring-hate-speech
3. Grid search was conducted in a random fashion to save time. If there are many sub-types of models to try (e.g. large, base), the parameters of the models will be kept frozen, the apparent winner will be kept for more extensive grid search.
4. YouTube comments are extracted by gathering the URLs of the top 5 most popular videos in order to extract their comments using YouTube Data API. This process was done manually for the POC purpose


Acknowledgements
- Inspired by Tina Huang's video: https://www.youtube.com/watch?v=kHOVWiZKpHM
- Project team members: Ana Gonzalez Ascaso, Alexander Gross, Cassady Cook, Maria Andrea Caicedo
