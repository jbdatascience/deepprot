<img align="center" width="150" height="150" src="logo.png">

# DeepProt

**A simple, universal API for machine learning on protein engineering.**



Quick Start
-----------

Train a protein model in four lines of Python.

```python
import deepprot

antibodies = dp.data.Dataset("cancer_cure.csv", X="seq", y="targetA")
dl = dp.data.DataLoader(antibodies, featurizer=deepprot.feat.KideraFactors())

cnn = dp.model.CNN()
cnn.fit(dl)
```

Use DeepProt's rich library of off-the-shelf models and featurizers:

```python

# Dozens of featurization schemes...
dl = dp.data.DataLoader(solubility_data, featurizer=deepprot.feat.ProtBert())
dl = dp.data.DataLoader(new_exp, featurizer=deepprot.feat.BLOSUMIndices())

# Generic architectures that resize to variable input under the hood.
model = dp.models.MLP()
model = dp.models.Transformer()
```


Getting Involved
----------------

- [`Slack`](https://join.slack.com/t/latch-world/shared_invite/zt-o4qhzu7r-uQMo_w_w_t~Oby4YPBYBgA): For discussions about development, questions about usage, and feature requests.
- [`GitHub Issues`](https://github.com/latchai/deepprot/issues): For reporting bugs.
- `kenny@latch.ai`: For questions about how to use DeepProt.
