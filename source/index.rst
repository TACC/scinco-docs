===============
What is SCINCO?
===============

The **Scinco project** at TACC provides a hosted interactive computing platform that augments and complements batch computing capabilities available today within science gateways. SCINCO combines container technology and state-of-the-art open source technologies such as Kubernetes and JupyterHub to deliver: 

* A hardened, production-grade platform that can support hundreds of projects running across thousands of nodes geographically distributed across dozens of academic clusters.
* Deep integration with advanced storage and computing resources available in existing science gateways.
* Sharing and publishing features allowing analyses to be packaged with data and shared privately with collaborators or disseminated to the community at large. Diverse areas of research, including Astronomy, Biology, Climate Science, Neuroscience, and various fields of Engineering will leverage the SCINCO platform to analyze big data, implement computational models, disseminate results and train the next generation of researchers.


============
Capabilities
============

Provides users with a customized Jupyter notebook server with access to TACC's storage and compute resources. Projects currently using JupyterHub at TACC are Designsafe-CI_ , Hobby Eberly Dark Energy Experiment (HETDEX_) and DARPA SHADE_. 

.. _Designsafe-CI: https://www.designsafe-ci.org 
.. _HETDEX: https://mcdonaldobservatory.org/research/telescopes/HET
.. _SHADE: https://www.shade-aie.org

==========
Components
==========

At its core, the Scinco architecture utilizes a customized **JupyterHub** version, an open-source, cloud-based Jupyter project that allows users to access notebook servers running on remote machines. Scinco incorporates multitenancy or logically separated instances of the platform so that individual projects can configure various aspects of the notebook servers and data made available to their users based on their individual project needs.
Basic components of Scinco are:

* OAuth-based Authenticator Plugin
* JupyterHub
* Customized notebook server images
* Administrative Portal

====================
Scinco Publications
====================
* Jamthe, A.; Stubbs, J.; Packard, M.; Chuah, J.; Looney, J.; Curbelo & Gilbert, C. (2021). Enriching scientific and interactive computing with project SCINCO: JupyterHub on Kubernetes. In Gateways 2021
* Stubbs, J., Looney, J., Poindexter, M., Chalhoub, E., Zynda, G., Ferlanti, E., Vaughn, M., Fonner, J., & Dahan, M. (2020). Integrating Jupyter into Research Computing Ecosystems: Challenges and Successes in Architecting JupyterHub for Collaborative Research Computing Ecosystems. In Practice and Experience in Advanced Research Computing (pp. 91–98). Association for Computing Machinery.