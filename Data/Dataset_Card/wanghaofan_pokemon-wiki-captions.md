---
dataset_info:
  features:
  - name: image
    dtype: image
  - name: name_en
    dtype: string
  - name: name_zh
    dtype: string
  - name: text_en
    dtype: string
  - name: text_zh
    dtype: string
  splits:
  - name: train
    num_bytes: 117645424.0
    num_examples: 898
  download_size: 117512478
  dataset_size: 117645424.0
---
# Dataset Card for Pokémon wiki captions

This project is inspired by [pokmon-blip-captions](https://huggingface.co/datasets/lambdalabs/pokemon-blip-captions), where the captions are all generated by pre-trained BLIP without any manual effort.
However, the quality and accuracy of their captions are not satisfactory enough, which leaves it known whether better captions lead to better results. This motivates our dataset.


# Example

![pk1.jpg](https://storage.googleapis.com/kagglesdsdata/datasets/1392907/2309103/Pokemon%20Dataset/aipom.png?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20221208%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20221208T155930Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=4b9c507a546d5b4517621ad440b274a50c88b3270e254eb1146098026fa5fe68e1f7e9699e1554802cc7bd6512ed39612ab63cf1da0d77957567d9ec4d7df8b0a5137ecdb371142cbbb00c966552599366608382c0381b46dc92dbc734bd72d62bba99e9c1efa45f498c4bdc1bf4b650e6275e3cd4467d6fa8dfe4dc57754b61b66f557b8ce2f03d03a6fa81258c7c330074a30a353a27f2436e1f79d0d19289008b601203fa8dd8da70e6de931ad79afa91134ac94695cbd3c8c09f6919c4144944ad3233314a9148a5f752c1f8b940a30bd7ade90844f9194454cae945da96f077fbc533c2154f0d4eb85df504426ad4b3426a63259cd5e69a379ac515b292)
> General attribute, looks like a little monkey, body color is composed of purple and beige, the end of the tail is like a hand

![pk2.jpg](https://storage.googleapis.com/kagglesdsdata/datasets/1392907/2309103/Pokemon%20Dataset/arbok.png?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20221208%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20221208T155930Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=42e8cf9eb3af2dac09ca3cfd72a2555c31af543b9b26be79933c7cd5586c8475a64246c5221a3815fb99502acfa8de20c029fe045568fda7c2582ff4f1a0d61423d5aa879d93c5d6331b7993803f25a6287b0ff8f8a8a3ab6bc947a3fe92db4c4551a2698eed46e73c93372bf1aa815268864377b581dafab7989ee757e67d91c126524cb640761758922f1039b4858f5bd7abe8c68fec6939469fe2116f9c6ade26a5d6120168a183f34e517e8d1e2f6873adbf54ad1db946c524894ac0a6945b9a92cb65577fe8b7c5a25aefe797a9b83398fba4407d6e7e2651c83ef97910c15ca1ff7e6075522004f8f776cd6acd014a78ce10010bc4c736eb9194602e81)
> Poisonous attributes, it looks like a huge purple cobra, with black stripes on its body, small head, and triangular eyes


# Properties

All 898 images are from [The Complete Pokemon Images Data Set](https://www.kaggle.com/datasets/arenagrenade/the-complete-pokemon-images-data-set?resource=download) in Kaggle with size 475x475. Each image is accompanied with corresponding 
pokemon name and its detailed description from [Pokemon Wiki](https://wiki.52poke.com/wiki/%E4%B8%BB%E9%A1%B5), English and Chinese captions are provided. Human efforts are also involved to revise.

# How to use
```
from datasets import load_dataset

dataset = load_dataset("wanghaofan/pokemon-wiki-captions")
```

The dataset is formatted as below. For each row the dataset contains `image`, `name_en`, `name_zh`, `text_en` and `text_zh` keys. `image` is a varying size PIL jpeg, `name` is the name of pokemon, and `text` is the accompanying text caption. Only a train split is provided.

```
DatasetDict({
    train: Dataset({
        features: ['image', 'name_en', 'name_zh', 'text_en', 'text_zh'],
        num_rows: 898
    })
})

```

# Citation
If you use this dataset in your work, please cite it as:

```
@misc{wanghaofan2022pokemon,
      author = {Haofan Wang},
      title = {Pokemon wiki captions},
      year={2022},
      howpublished= {\url{https://huggingface.co/datasets/wanghaofan/pokemon-wiki-captions/}}
} 
```