# TADNE sample images

Images generated by the [TADNE model](https://huggingface.co/hysts/TADNE).

## Note

- `prediction_results/anime-face-detector`
    - https://github.com/hysts/anime-face-detector
    - YOLOv3 + HRNetV2
- `prediction_results/deepdanbooru`
    - https://github.com/KichangKim/DeepDanbooru
    - `model-resnet_custom_v3.h5`
- `prediction_results/deepdanbooru/intermediate_features`
    - Output by the following model
    - 4096-dim

```python
def create_model() -> tf.keras.Model:
    path = huggingface_hub.hf_hub_download('hysts/DeepDanbooru',
                                           'model-resnet_custom_v3.h5',
                                           use_auth_token=TOKEN)
    model = tf.keras.models.load_model(path)
    model = tf.keras.Model(model.input, model.layers[-4].output)
    layer = tf.keras.layers.GlobalAveragePooling2D()
    model = tf.keras.Sequential([model, layer])
    return model
```

