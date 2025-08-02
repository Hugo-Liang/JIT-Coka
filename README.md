# JIT-Coka

**Note:** 
1. All supplemental materials for the paper can be found in the **appendix** folder.
2. The necessary scripts of **run.py** and **model.py** under the **JITCoka/concat/** folder, as well as our trained checkpoint of JIT-Coka will be released soon.

#### 1. Project Description
Replication package for the paper entitled: JIT-Coka: An Improved Framework for Just-in-Time Defect Prediction and Localization Using Fused Features of Code Change


#### 2. System Environment
    CPU：Intel(R) Xeon(R) Gold 5118
    
    RAM：100 GB 
    
    GPU：NVIDIA Tesla P40 24G
    
    OS：CentOS 7.6


#### 3. Environment Settings
```conda create --name JIT-Coka python=3.8.12```

```conda activate JIT-Coka```

```pip install torch==1.9.0+cu111 -f https://download.pytorch.org/whl/torch_stable.html```

```pip install -r requirements.txt```


#### 4. Data and Pre-trained Model Files Preparation
1. Extract the data used to train and evaluate JIT-Coka via ```tar -zxvf data/jitcoka.tar.gz```.
2. 
**Note:** These files are the same as those used to train and evaluate JIT-Smart.


2. Manually download the **added_tokens.json, config.json, merges.txt, pytorch_model.bin, special_tokens_map.json, tokenizer_config.json, and vocab.json** from [Hugging Face-CodeT5](https://huggingface.co/Salesforce/codet5-base/tree/main), upload them to the **models/codet5_base/** folder.


#### 5. Run JIT-Coka
**1. Test using our trained checkpoint.**

Comment out the first line in the **train_jitcoka.sh** file, and directly test JIT-Coka via ```bash train_jitcoka.sh```

**2. Train and test JIT-Coka from scratch.**

```bash train_jitcoka.sh```


### Get Involved
Please create a GitHub issue if you have any questions, suggestions, requests or bug-reports.