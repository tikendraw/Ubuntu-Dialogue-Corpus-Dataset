

# Understanding The Ubuntu Dialogue Corpus Data

[Dataset Here](https://paperswithcode.com/dataset/ubuntu-dialogue-corpus#:~:text=Ubuntu%20Dialogue%20Corpus%20(UDC)%20is,large%20amounts%20of%20unlabeled%20data.)

Ubuntu Dialogue Corpus (UDC) is a dataset containing almost 1 million multi-turn dialogues, with a total of over 7 million utterances and 100 million words. This provides a unique resource for research into building dialogue managers based on neural language models that can make use of large amounts of unlabeled data. The dataset has both the multi-turn property of conversations in the Dialog State Tracking Challenge datasets, and the unstructured nature of interactions from microblog services such as Twitter.

## Why am I here?

One day (Jan-24-2023), I thought "Let't make a chatbot" I had limited data, So I looked in my computer to see if I have downloaded any chat datasets to work with. I found this `Ubuntu Dialogue Corpus`. It is Pretty big dataset to work with.

I installed Polars `!pip install polars` , It is alot faster(10x-22x) than pandas and uses less memory. It was a perfect choice. I started Readint through the data.
Found how the Data is structured . Wrote a function to visualize the data in a chat format. Things were going good. I Started reading the text. I got to Know things:

1. All Conversations were truncated to 3 entries. (So probabily no complete answers)
2. It is a very specific domain conversation .
3. Apart from the fact it is written by actual human, it is surving no purpose to me atleast.
4. There isn't any Information to learn or personality to capture.(too technical)

So after some time I stopped the digging through this data. I will find another one.

Seems Like Entry with some `dialogueID` with no `To` value are questions asked by `from` guy and in the same `dialogueID` and Entry with `to` values are reply from `from` guy

![Screenshot from 2023-01-24 16-08-13.png](attachment:1eed13f6-6f44-426f-83a0-edd339dd6961.png)

* Entries with same `dialogueID` are one  single post
* Entries with no `to` values are Questions
* Entries with any values in `to` are answers by `from`