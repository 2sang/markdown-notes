## Keras notes

#### How can I obtain the output of an intermediate layer? - [Keras Official docs](https://keras.io/getting-started/faq/#how-can-i-obtain-the-output-of-an-intermediate-layer)
One simple way is to create a new Model() that will output the layers that you are insterested in.
```python
from keras.models import Model

model = ...  # create the original model

layer_name = 'my_layer'
intermediate_layer_model = Model(inputs=model.input,
                                 outputs=model.get_layer(layer_name).output)
intermediate_output = intermediate_layer_model.predict(data)
```


