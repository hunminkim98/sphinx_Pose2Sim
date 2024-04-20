.. image:: https://github.com/perfanalytics/pose2sim/actions/workflows/continuous-integration.yml/badge.svg?branch=main
    :target: https://github.com/perfanalytics/pose2sim/actions/workflows/continuous-integration.yml

.. image:: https://badge.fury.io/py/Pose2Sim.svg
    :target: https://badge.fury.io/py/Pose2Sim

.. image:: https://static.pepy.tech/badge/pose2sim
    :target: https://pepy.tech/project/pose2sim

.. image:: https://img.shields.io/github/stars/perfanalytics/pose2sim
    :target: https://github.com/perfanalytics/pose2sim/stargazers

.. image:: https://img.shields.io/github/forks/perfanalytics/pose2sim
    :target: https://GitHub.com/perfanalytics/pose2sim/forks

.. image:: https://img.shields.io/github/issues/perfanalytics/pose2sim
    :target: https://github.com/perfanalytics/pose2sim/issues

.. image:: https://img.shields.io/github/issues-closed/perfanalytics/pose2sim
    :target: https://GitHub.com/perfanalytics/pose2sim/issues?q=is%3Aissue+is%3Aclosed

.. image:: https://joss.theoj.org/papers/a31cb207a180f7ac9838d049e3a0de26/status.svg
    :target: https://joss.theoj.org/papers/a31cb207a180f7ac9838d049e3a0de26

.. image:: https://zenodo.org/badge/501642916.svg
    :target: https://zenodo.org/doi/10.5281/zenodo.10658947

.. image:: https://img.shields.io/badge/License-BSD_3--Clause-blue.svg
    :target: https://opensource.org/licenses/BSD-3-Clause


Pose2Sim
========

.. note:: Please set undistort_points and handle_LR_swap to false for now since it currently leads to inaccuracies. I'll try to fix it soon.

.. note:: **News: Version 0.8:**

   - **Automatic camera synchronization is now supported!**
   - **Other recently added features**: Multi-person analysis, Blender visualization, Marker augmentation, Automatic batch processing.

To upgrade, use:

.. code-block:: bash

    pip install pose2sim --upgrade

Pose2Sim provides a workflow for 3D markerless kinematics, as an alternative to the more usual marker-based motion capture methods. It aims to provide a free tool to obtain research-grade results from consumer-grade equipment. Any combination of phone, webcam, GoPro, etc. can be used.

Pose2Sim stands for "OpenPose to OpenSim", as it uses OpenPose inputs (2D keypoints coordinates obtained from multiple videos) and leads to an OpenSim result (full-body 3D joint angles). Other 2D pose estimators such as BlazePose (MediaPipe), DeepLabCut, AlphaPose, can now be used as inputs.

If you can only use one single camera and don't mind losing some accuracy, please consider using `Sports2D <https://github.com/davidpagnon/Sports2D>`_.

.. image:: https://raw.githubusercontent.com/perfanalytics/pose2sim/main/Content/Pose2Sim_workflow.jpg
    :width: 760
    :alt: Pose2Sim Workflow

.. figure:: https://github.com/perfanalytics/pose2sim/blob/main/Content/Activities_verylow.gif?raw=true
   :width: 760
   :alt: Activities

   Other more or less challenging tasks and conditions.


.. note:: As always, I am more than happy to welcome contributors (see "How to contribute").

Pose2Sim releases:
==================

- ✅ **v0.1 (08/2021):** Published paper
- ✅ **v0.2 (01/2022):** Published code
- ✅ **v0.3 (01/2023):** Supported other pose estimation algorithms
- ✅ **v0.4 (07/2023):** New calibration tool based on scene measurements
- ✅ **v0.5 (12/2023):** Automatic batch processing
- ✅ **v0.6 (02/2024):** Marker augmentation, Blender visualizer
- ✅ **v0.7 (03/2024):** Multi-person analysis
- ✅ **v0.8 (04/2024):** New synchronization tool
- 🔲 **v0.9:** Calibration based on keypoint detection, Handling left/right swaps, Correcting lens distortions
- 🔲 **v0.10:** Graphical User Interface
- 🔲 **v1.0:** First accomplished release

How to cite and how to contribute
=================================

How to cite
-----------

If you use this code or data, please cite `Pagnon et al., 2022b <https://doi.org/10.21105/joss.04362>`_, `Pagnon et al., 2022a <https://www.mdpi.com/1424-8220/22/7/2712>`_, or `Pagnon et al., 2021 <https://www.mdpi.com/1424-8220/21/19/6530>`_.

.. code-block::

    @Article{Pagnon_2022_JOSS,
      AUTHOR = {Pagnon, David and Domalain, Mathieu and Reveret, Lionel},
      TITLE = {Pose2Sim: An open-source Python package for multiview markerless kinematics},
      JOURNAL = {Journal of Open Source Software},
      YEAR = {2022},
      DOI = {10.21105/joss.04362},
      URL = {https://joss.theoj.org/papers/10.21105/joss.04362}
    }

    @Article{Pagnon_2022_Accuracy,
      AUTHOR = {Pagnon, David and Domalain, Mathieu and Reveret, Lionel},
      TITLE = {Pose2Sim: An End-to-End Workflow for 3D Markerless Sports Kinematics—Part 2: Accuracy},
      JOURNAL = {Sensors},
      YEAR = {2022},
      DOI = {10.3390/s22072712},
      URL = {https://www.mdpi.com/1424-8220/22/7/2712}
    }

    @Article{Pagnon_2021_Robustness,
      AUTHOR = {Pagnon, David and Domalain, Mathieu and Reveret, Lionel},
      TITLE = {Pose2Sim: An End-to-End Workflow for 3D Markerless Sports Kinematics—Part 1: Robustness},
      JOURNAL = {Sensors},
      YEAR = {2021},
      DOI = {10.3390/s21196530},
      URL = {https://www.mdpi.com/1424-8220/21/19/6530}
    }

How to contribute and to-do list
--------------------------------

I would happily welcome any proposal for new features, code improvement, and more!
If you want to contribute to Pose2Sim, please see `this issue <https://github.com/perfanalytics/pose2sim/issues/40>`_.
You will be proposed a to-do list, but please feel absolutely free to propose your own ideas and improvements.

**Main to-do list**

- ✅ **Synchronization**  
- 🔲 **Graphical User Interface**  
- 🔲 **Self-calibration based on keypoint detection**

Acknowledgements
----------------

* Supervised my PhD: `@lreveret <https://github.com/lreveret>`_ (INRIA, Université Grenoble Alpes), and `@mdomalai <https://github.com/mdomalai>`_ (Université de Poitiers).
* Provided the Demo data: `@aaiaueil <https://github.com/aaiaueil>`_ from Université Gustave Eiffel.
* Tested the code and provided feedback: `@simonozan <https://github.com/simonozan>`_, `@daeyongyang <https://github.com/daeyongyang>`_, `@ANaaim <https://github.com/ANaaim>`_, `@rlagnsals <https://github.com/rlagnsals>`_
* Submitted various accepted pull requests: `@ANaaim <https://github.com/ANaaim>`_, `@rlagnsals <https://github.com/rlagnsals>`_
* Provided a code snippet for Optitrack calibration: `@claraaudap <https://github.com/claraaudap>`_ (Université Bretagne Sud).
* Issued MPP2SOS, a (non-free) Blender extension based on Pose2Sim: `@carlosedubarreto <https://github.com/carlosedubarreto>`