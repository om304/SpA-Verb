# SpA-Verb
**Semantic similarity evaluation resource for English verbs**

This repository contains the resource introduced in the paper: 

Olga Majewska, Diana McCarthy, Jasper van den Bosch, Nikolaus Kriegeskorte, Ivan Vulić, and Anna Korhonen. 2020.  __Spatial Multi-Arrangement for Clustering and Multi-way Similarity Dataset Construction__. In Proceedings of LREC 2020.

## **Resource description**

The resource comprises two types of verb data: **17 relatedness-based verb classes** and a **verb similarity dataset** containing similarity scores for **29,721 unique verb pairs** and 825 target verbs. Note that the scores are scaled Euclidean distances, therefore smaller scores correspond to greater similarity, while larger scores reflect a greater semantic distance (i.e. dissimilarity). We also make available evaluation files including pairwise similarity scores collected for each class, allowing for analyses and evaluation on chosen semantic classes and meaning domains (e.g., verbs of motion, verbs of communication, verbs of change). These two data types correspond to the two phases of our dataset construction methodology:

* **Phase 1: Rough semantic clustering** 

Human annotators are presented with a 825-verb sample and asked to group them into broad classes, putting similar and related words in the same groups. The result of this phase are 17 semantic classes, used as input to Phase 2.

* **Phase 2: Spatial similarity judgments**

Semantic verb classes from Phase 1 are presented individually around a circular 2D arena visible on the computer screen. Human annotators are asked to arrange the verbs in the arena based on the similarity of their meaning, putting similar verbs close together and dissimilar ones further apart.

Please refer to the paper for details of each phase and the rationale behind our methodology.

## **Data**

The directory includes the following files and folders:

* 17verb_classes.txt - semantic verb classes resulting from Phase 1 
* SpA-Verb.txt       - the complete similarity dataset resulting from Phase 2, with scores for 29,721 English verb pairs
* SpA-Verb-THR.txt   - the thresholded subset of the entire dataset, including scores from classes with Spearman's IAA > 0.3
* Phase 2/           - folder containing files with pairwise similarity scores for each of the 17 semantic classes 

## **Data format**

In the following we describe the format of each file.

* 17verb_classes.txt

A tab-separated plain text file including the 17 semantic verb classes resulting from Phase 1. The classes are numbered (1-17), in the format one class per line.

* SpA-Verb.txt

A tab-separated plain text file including similarity scores for 29,721 English verb pairs. 
**Important**: the similarity scores are scaled Euclidean distances, as measured in Phase 2 in the 2D arena, therefore smaller scores correspond to greater similarity, while larger scores reflect a greater semantic distance (i.e. dissimilarity).

  Word1: The first verb of the pair.

  Word2: The second verb of the pair.

  Score: The SpA-Verb similarity score. The similarity scores are scaled Euclidean distances (the lower the score, the more similar the two words are). Please take that into account when running Spearman rank-based correlation analyses.

* SpA-Verb-THR.txt

A tab-separated plain text file including similarity scores for the subset of 10,371 pairs from classes where Spearman's correlation-based inter-annotator agreement was higher than 0.3. The format is analogous to SpA-Verb.txt

* Phase 2/

  class1.txt
  
  class2.txt
  
  class3.txt
  
  class4.txt
  
  class5.txt
  
  class6.txt
  
  class7.txt
  
  class8.txt
  
  class9.txt
  
  class10.txt
  
  class11.txt
  
  class12.txt
  
  class13.txt
  
  class14.txt
  
  class15.txt
  
  class16.txt
  
  class17.txt

Each plain text file is tab-separated and follows the same format as SpA-Verb.txt. Below we provide examples of verbs in each class to help identify the meaning domain on which the class in question focuses (e.g., motion verbs: _run_, _swim_, _skip_, communication verbs: _ask_, _inquire_, _argue_, cooking verbs: _bake_, _broil_, _fry_, etc.). Please refer to the paper for more details and examples.

 Class 1: _beat, punch, smash, slap_
 
 Class 2: _accuse, condemn, forbid, blame_
 
 Class 3: _accelerate, decrease, shrink, increase_
 
 Class 4: _achieve, aim, tackle, accomplish_
 
 Class 5: _acquire, have, keep, borrow_
 
 Class 6: _dismay, frustrate, upset, irritate_
 
 Class 7: _ask, confess, discuss, inquire_
 
 Class 8: _approve, desire, prefer, respect_
 
 Class 9: _calculate, analyze, predict, guess_
 
 Class 10: _climb, jump, roam, slide_
 
 Class 11: _bake, grate, slice, broil_
 
 Class 12: _cough, gulp, inhale, sniff_
 
 Class 13: _chirp, hoot, roar, whistle_
 
 Class 14: _build, fasten, mend, restore_
 
 Class 15: _drag, fling, haul, toss_
 
 Class 16: _demolish, erode, wreck, disintegrate_
 
 Class 17: _glance, observe, perceive, look_
 
 ## License
 
 All data on this page are made available under the Creative Commons Attribution (CC BY) license.
