---
dataset_info:
  features:
  - name: instruction
    dtype: string
  - name: instances
    list:
    - name: instruction_with_input
      dtype: string
    - name: input
      dtype: string
    - name: constraints
      dtype: string
    - name: output
      dtype: string
  - name: reformulations
    list:
    - name: instruction
      dtype: string
    - name: instruction_with_input
      dtype: string
    - name: input
      dtype: string
    - name: output
      dtype: string
  splits:
  - name: train
    num_bytes: 144282712
    num_examples: 66010
  download_size: 57715606
  dataset_size: 144282712
---
# Dataset Card for Unnatural Instructions (Full data)
This info comes from the **Unnatural Instructions GitHub [repo](https://github.com/orhonovich/unnatural-instructions/)**.

Unnatural Instructions is a dataset of instructions automatically generated by a Large Language model.
See full details in the paper: "[Unnatural Instructions: Tuning Language Models with (Almost) No Human Labor](https://arxiv.org/abs/2212.09689)"

## 🗃️ Content
It contains the full 240,670 Unnatural Instructions (instruction-input-output triplets) examples. It was constructed by expanding the core data with automatically generated instruction paraphrases.

## 📄 Format
### Full data
It has the same structure as [Core Data](https://huggingface.co/datasets/mrm8488/unnatural-instructions-core), but with one additional field - `reformulations`. `reformulations` is an array of JSON objects, each corresponds to an automatically generated paraphrase for the given instruction. Each reformulation contains the fields:
- `instruction`: A paraphrase of the original instruction
- `input`: An input for the task described by the `instruction`
- `instruction_with_input`: The paraphrased instruction concatenated with the `input`
- `output`: The output of executing `instruction` with the given `input`


## 📘 Citation
If you make use of Unnatural Instructions, please cite the following paper:
```
@misc{honovich2022unnatural,
      title = {Unnatural Instructions: Tuning Language Models with (Almost) No Human Labor},
      author = {Honovich, Or and Scialom, Thomas and Levy, Omer and Schick, Timo},
      url = {https://arxiv.org/abs/2212.09689},
      publisher = {arXiv},
      year={2022}
}
```

[More Information needed](https://github.com/huggingface/datasets/blob/main/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)