# ROLEBENCH 

ROLEBENCH is a framework for evaluating the performance of Role-Prompting across different datasets and Large Language Models. 

## Supported models
- Llama3-8B Instruct 
- Phi-3 mini-4K Instruct
- Mistral-7B Instruct
- Gemma-7B Instruct

## Datasets
- BoolQ (validation split - 3270 samples)
- COMMONSENSEQA (validation split - 1221 samples)
- iwslt2017-en-fr dataset (validation split - 890 samples)
- samsum dataset (test split - 819 samples)

## Prompt Template 
```bash

BoolQ - Based on the passage:'{passage}'\nAnswer True/False to the question: '{question}' as an Omniscient person.

COMMONSENSEQA - Choose the answer as a critical thinker.\n{question}\n{opt1}. {text1}\n{opt2}. {text2}\n{opt3}. {text3}\n{opt4}. {text4}\n{opt5}. {text5}

IWSLT2017en-fr - Translate '{eng_text}' to french as a Translator.

SamSum - Summarise the Dialogue: {dialogue} as a Storyteller.
```


## Results
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>BoolQ</th>
      <th>COMMONSENSEQA</th>
      <th>IWSLT2017en-fr</th>
      <th>SamSum</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Llama3</td>
      <td>Accuracy = 0.8507<br>F1 score = 0.8793</td>
      <td>Accuracy = 0.7371</td>
      <td>BLEU = 0.2399<br>METEOR = 0.5436</td>
      <td>Rouge1 = 0.1725<br>RougeL = 0.1229</td>
    </tr>
    <tr>
      <td colspan="4"></td>
    </tr>
    <tr>
      <td rowspan="2">Phi-3</td>
      <td>Accuracy = 0.8113<br>F1 score = 0.8344</td>
      <td>Accuracy = 0.7068</td>
      <td>BLEU = 0.1928<br>METEOR = 0.4950</td>
      <td>Rouge1 = 0.1383<br>RougeL = 0.0951</td>
    </tr>
    <tr>
      <td colspan="4"></td>
    </tr>
    <tr>
      <td rowspan="2">Mistral-7B</td>
      <td>Accuracy = 0.8281<br>F1 score = 0.8548</td>
      <td>Accuracy = 0.6490</td>
      <td>BLEU = 0.1507<br>METEOR = 0.4763</td>
      <td>Rouge1 = 0.1359<br>RougeL = 0.0991</td>
    </tr>
    <tr>
      <td colspan="4"></td>
    </tr>
    <tr>
      <td rowspan="2">Gemma-7B</td>
      <td>Accuracy = 0.6288<br>F1 score = 0.5831</td>
      <td>Accuracy = 0.6288</td>
      <td>BLEU = 0.0940<br>METEOR = 0.3611</td>
      <td>Rouge1 = 0.1192<br>RougeL = 0.0793</td>
    </tr>
    <tr>
      <td colspan="4"></td>
    </tr>
  </tbody>
</table>

## Repository Structure
```bash

_llama3_role_all.ipynb -- Role prompting on all datasets using Llama3-8B Instruct model
|
|_phi3_role_all.ipynb -- Role prompting on all datasets using Phi-3 mini-4K Instruct model
|
|_mistral_role_all.ipynb -- Role prompting on all datasets using Mistral-7B Instruct model
|
|_Gemma_role_all.ipynb  -- Role prompting on all datasets using Gemma-7B Instruct model
|
|_Role_prompting____quantitaive_analysis.txt 
                  |_qualitative_analysis.txt 
```

## Contribution 
The project will always remain OPEN-SOURCE, further contributions involving new models and datasets, formulating new roles in the prompt templates are always welcome.

## References
if you find this work useful, please cite this repository:
- 






