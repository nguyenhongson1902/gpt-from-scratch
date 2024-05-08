# Building GPT from scratch
Ever since ChatGPT appeared, there was a boom in medium-to-large technological companies using LLMs to develop theirs applications. Not only tech, but it is also surprising when people from different disciplines also converse about ChatGPT on a day-to-day basis. Just like ChatGPT, there are a lot of other LLMs that are also based on transformer neural networks. And today, I will build a famous GPT (Generative Pre-trained Transformers) from scratch for the purpose of learning basic inner workings of LLMs.

In this repository, I will only consider the task of generating Shakespeare-like text for now. So the architecture will only contain the Decoder part of the Transformer.

## Installation
Create an Anaconda environment and install the necessary packages: ```torch 2.0.0```, ```python 3.10.10```

## Resources
- 1 NVIDIA RTX A5000 GPU with 24GB of RAM
- OS: Ubuntu 20.04.6 LTS

## Results
**Simple bigram model:**
```step: 0, train loss: 4.7305, val loss: 4.7241
step: 300, train loss: 2.8110, val loss: 2.8249
step: 600, train loss: 2.5434, val loss: 2.5682
step: 900, train loss: 2.4932, val loss: 2.5088
step: 1200, train loss: 2.4863, val loss: 2.5035
step: 1500, train loss: 2.4665, val loss: 2.4921
step: 1800, train loss: 2.4683, val loss: 2.4936
step: 2100, train loss: 2.4696, val loss: 2.4846
step: 2400, train loss: 2.4638, val loss: 2.4879
step: 2700, train loss: 2.4738, val loss: 2.4911



CEThik brid owindakis b, bth

HAPet bobe d e.
S:
O:3 my d?
LUCous:
Wanthar u qur, t.
War dXENDoate awice my.

Hastarom oroup
Yowhthetof isth ble mil ndill, ath iree sengmin lat Heriliovets, and Win nghir.
Swanousel lind me l.
HAshe ce hiry:
Supr aisspllw y.
Hentofu n Boopetelaves
MPOLI s, d mothakleo Windo whth eisbyo the m dourive we higend t so mower; te

AN ad nterupt f s ar igr t m:

Thin maleronth,
Mad
RD:

WISo myrangoube!
KENob&y, wardsal thes ghesthinin couk ay aney IOUSts I&fr y ce.
J
```
Estimated time: Very fast!

**Enhanced version with self-attention mechanism:**
```
step: 0, train loss: 4.4752, val loss: 4.4707
step: 500, train loss: 1.9090, val loss: 2.0132
step: 1000, train loss: 1.5512, val loss: 1.7361
step: 1500, train loss: 1.4027, val loss: 1.6109
step: 2000, train loss: 1.3142, val loss: 1.5586
step: 2500, train loss: 1.2456, val loss: 1.5258
step: 3000, train loss: 1.1877, val loss: 1.5049
step: 3500, train loss: 1.1353, val loss: 1.4994
step: 4000, train loss: 1.0842, val loss: 1.5040
step: 4500, train loss: 1.0299, val loss: 1.5114

Say we sweetly and so unavoided to marshall reg grain
Upon his own reason. Then last, I cannot say
The carge what laters I am an astinite-mornice man
it only to answer ease would play.

MENENIUS:
I not in the heavens
Ensachien if the wealth, since with spirit,
it were a pomper-stilch and victory in the nature,
To know himself; but, at I the prince's dagger,
It must be consumed, and death, you should fast,
That from them the prince a Junow thou hard;
And all where honourable see a best:
The minni
```
Estimated time: ~15 min (Notice the `val loss` is much lower compared to the simple version)

## To-do
- [x] Built a simple bigram language model
- [x] Built an enhanced model with self-attention mechanism
- [ ] Packed this app to Docker
- [ ] Completed the Encoder part of Transformer to apply cross-attention
- [ ] Quantized model to reduce model params without degrading the original performance
- [ ] Built a speech recognition model using Transformer
- [ ] Tried distributed training






