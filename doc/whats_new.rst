.. currentmodule:: imbalanced-learn

===============
Release history
===============

.. _changes_0_2:

Version 0.2
===========

Changelog
---------

Bug fixes
~~~~~~~~~

- Fixed a bug in :class:`under_sampling.NearMiss` which was not picking the right samples during under sampling for the method 3. By `Guillaume Lemaitre`_.
- Fixed a bug in :class:`ensemble.EasyEnsemble`, correction of the `random_state` generation. By `Guillaume Lemaitre`_ and `Christos Aridas`_.
- Fixed a bug in :class:`under_sampling.RepeatedEditedNearestNeighbours`, add additional stopping criterion to avoid that the minority class become a majority class or that a class disappear. By `Guillaume Lemaitre`_.
- Fixed a bug in :class:`under_sampling.AllKNN`, add stopping criteria to avoid that the minority class become a majority class or that a class disappear. By `Guillaume Lemaitre`_.
- Fixed a bug in :class:`under_sampling.CondensedNeareastNeigbour`, correction of the list of indices returned. By `Guillaume Lemaitre`_.
- Fixed a bug in :class:`ensemble.BalanceCascade`, solve the issue to obtain a single array if desired. By `Guillaume Lemaitre`_.

New features
~~~~~~~~~~~~

- Added AllKNN under sampling technique. By `Dayvid Oliveira`_.

API changes summary
~~~~~~~~~~~~~~~~~~~

- Two base classes :class:`BaseBinaryclassSampler` and :class:`BaseMulticlassSampler` have been created to handle the target type and raise warning in case of abnormality. By `Guillaume Lemaitre`_ and `Christos Aridas`_.

Enhancement
~~~~~~~~~~~

- Added support for bumpversion. By `Guillaume Lemaitre`_.
- Validate the type of target in binary samplers. A warning is raised for the moment. By `Guillaume Lemaitre`_ and `Christos Aridas`_.

Documentation changes
~~~~~~~~~~~~~~~~~~~~~

- Added doctest in the documentation. By `Guillaume Lemaitre`_.

.. _changes_0_1:

Version 0.1
===========

Changelog
---------

API
~~~

- First release of the stable API. By `Fernando Nogueira`_, `Guillaume Lemaitre`_, `Christos Aridas`_, and `Dayvid Oliveira`_.

New methods
~~~~~~~~~~~

* Under-sampling
    1. Random majority under-sampling with replacement
    2. Extraction of majority-minority Tomek links
    3. Under-sampling with Cluster Centroids
    4. NearMiss-(1 & 2 & 3)
    5. Condensend Nearest Neighbour
    6. One-Sided Selection
    7. Neighboorhood Cleaning Rule
    8. Edited Nearest Neighbours
    9. Instance Hardness Threshold
    10. Repeated Edited Nearest Neighbours

* Over-sampling
    1. Random minority over-sampling with replacement
    2. SMOTE - Synthetic Minority Over-sampling Technique
    3. bSMOTE(1 & 2) - Borderline SMOTE of types 1 and 2
    4. SVM SMOTE - Support Vectors SMOTE
    5. ADASYN - Adaptive synthetic sampling approach for imbalanced learning

* Over-sampling followed by under-sampling
    1. SMOTE + Tomek links
    2. SMOTE + ENN

* Ensemble sampling
    1. EasyEnsemble
    2. BalanceCascade

.. _Guillaume Lemaitre: https://github.com/glemaitre
.. _Christos Aridas: https://github.com/chkoar
.. _Fernando Nogueira: https://github.com/fmfn
.. _Dayvid Oliveira: https://github.com/dvro
