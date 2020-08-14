# Tensorflow

## Tensor

| rank                                                                                                                                            | object                                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0                                                                                                                                               | scalar                                                                                                                                              |
| 1                                                                                                                                               | vector                                                                                                                                              |
| 2                                                                                                                                               | <img src="https://mathworld.wolfram.com//images/equations/TensorRank/Inline11.gif" class="inlineformula" width="35" height="15" alt="N×N" /> matrix |
| <img src="https://mathworld.wolfram.com//images/equations/TensorRank/Inline12.gif" class="inlineformula" width="22" height="15" alt="&gt;=3" /> | tensor                                                                                                                                              |

Why is it called TensorFlow?

- "stateful dataflow graphs"
- Sessions provides execution environments for Graphs to flow
- Tensors trained via mutation of Variables
- Models asked to make Predictions after Training

## Keras

- Saving checkpoints while training model in Keras

  ```py
  filepath = "saved-model-{epoch:02d}-{val_acc:.2f}.hdf5"
  checkpoint = keras.callbacks.ModelCheckpoint(filepath, monitor='val_acc', verbose=1, save_best_only=False, mode='max')
  ```

- https://github.com/yazdipour/SRU-deeplearning-workshop/
- np.squeeze > Remove single-dimensional entries from the shape of an array.
- model = Sequential() > Standard MLP Model
- model.add(Dense(64 `hyperparameter - hidden neuron` , activation='relu', input=25 `input params - only for first layer`))
- Usually add softmax at the last layer `model.add(Dense(activiation='softmax'))` / softmax will normalize the result for us.
- model.summery() > will print model structure > ex. FC | (NONE `is mini_batch`, 64)
- `model.compile(loss=,optimizer=,metrics=,validation_split=0.2)`
