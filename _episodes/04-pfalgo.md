---
title: "The Particle Flow algorithm and reconstruction of other objects"
teaching: 20
exercises: 0
questions:
- "What is the particle flow algorithm?"
- "What are the key aspects to remember about how PF works?"
- "How can PF can be used to build physics objects?"
objectives:
- Learn the basic aspects of the PF algorithm.
- Get the ide of how physics objects are built using the PF algorithm
keypoints:
- The PF algorithm aims at reconstructing and identifying all stable particles in the event, which can be later used to build other physics objects.
---

## Overview

In the last episode, you learned about how electromagnetic objects are reconstructed using methods like clustering and linking of tracks with ECAL energy deposits.  These actions are essential parts of the so-called **Particle Flow** (PF) algorithm.


<img src="../fig/pflow.png" width="600">

The particle-flow algorithm aims at reconstructing and identifying all stable particles in the event, i.e., electrons, muons, photons, charged hadrons and neutral hadrons, with a thorough combination of all CMS sub-detectors towards an optimal determination of their direction, energy and type. This list of individual particles is then used, as if it came from a Monte-Carlo event generator, to build jets (from which the quark and gluon energies and directions are inferred), to determine the missing transverse energy (which gives an estimate of the direction and energy of the neutrinos and other invisible particles), to reconstruct and identify taus from their decay products and more. 

## Clustering, blocking and linking

To dig deeper into the logic of the main tasks needed in a PF algorithm for reconstruction, please read [these slides](../files/Askew_Clustering_Block.pdf) from one of our CMS colleages.  Answer the questions below in our [assignment form](https://forms.gle/sMyuLFiYJWRsUAew6).

**Question #5**:
What does the energy of a clustering seed in the calorimeters need to be? 

**Question #6**:
What are blocks?

## Particles and corrections

At this point you must have a pretty good picture of how the different physics objects (and their final incarnation as particles) are made.

For instance, in the image below, where egamma (electrons and photons) objects (in red and blue), inner tracks (black) and muon chambers tracks (also called *standalone* in green) are depicted, one can infer the possibility (particle hypothesis) of building  **global muons**.

<img src="../fig/muons.png" width="600">


Note that the global muon on the left might not be isolated (there is a lot of track activity around), while the one on the right does seem to be an isolated one (of course, muons can also leave energy in the calorimeters).  Following a jet clustering algorithm, the bulk of activity on the left could be identified as a jet.  Most algorithms in CMS use PF objects.

Finally, these physics objects may need corrections.  Check out these example for ECAL cell calibrations needed for all ECAL clusters:

<img src="../fig/clustercalib.png" width="600">

As it was mentioned in the beginning, a list of physics object can be found in this [guide](https://opendata.cern.ch/docs/cms-physics-objects-2011#list-of-cms-physics-objects) from the CODP.  There, one can also find extended references.



{% include links.md %}
