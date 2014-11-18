hml-xgboost
===========

``hml-xgboost`` is a ``Docker`` container where the ``xgboost``
software has been packaged up.

## Installation

Once [docker](https://docs.docker.com/installation/) has been
installed, ``xgboost`` can be installed like so:

```sh
$ docker pull higgsml/xgboost:latest
```

## Usage

```sh
$ docker run -it higgsml/xgboost

[docker] hml-validate -build=0 $BUILD_DIR
::: higgsml-validate...

=== code submission #1/1 (code)...
::: run prediction...
::: higgs-ml [prediction]...
::: args: /higgsml/data/test.csv /tmp/higgsml-validate-740964401/code/trained.dat /tmp/higgsml-validate-740964401/code/.higgsml-work/submission.csv
/higgsml/data/test.csv
test: punits are ['tau', 'lep', 'jet_leading', 'jet_subleading', 'met']
/tmp/higgsml-validate-740964401/code/python/physics.py:38: RuntimeWarning: invalid value encountered in sqrt
  self.m_tri = np.sqrt(self.E_tri**2 - self.p_x**2 - self.p_y**2)
/tmp/higgsml-validate-740964401/code/python/physics.py:45: RuntimeWarning: invalid value encountered in sqrt
  self.p_y**2 - self.p_z**2)
31 psets discovered
finish making features, shape=(550000, 168)
finished writing into prediction file
::: higgs-ml [prediction]... [ok]
::: run prediction... [ok] (delta=25.527732041s)
=== code submission #1/1 (code)... [ok] (delta=25.535303896s)
```
