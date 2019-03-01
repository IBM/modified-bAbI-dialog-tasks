Modified Dialog bAbI tasks data
-----------------------------------------------------------------------
Adaptation of the "Dialog bAbI tasks data" dataset released by Facebook, available at https://research.fb.com/downloads/babi/, under the CC BY 3.0 Unported license, available at https://creativecommons.org/licenses/by/3.0/legalcode.

This directory contains modified-bAbI dialog tasks, an extension of original-bAbI dialog tasks, as described in the paper "Learning End-to-End Goal-Oriented Dialog with maximal User task success and minimal Human Agent use" by Janarthanan Rajendran, Jatin Ganhotra and Lazaros Polymenakos (arxiv link coming soon), accepted at TACL.
We modify the original-bAbI dialog tasks, by removing and replacing certain user behaviors from the training and validation data. The test set is left untouched. This simulates a scenario where some new user behaviors arise during the test (deployment) time that were not seen during the training and hence allows us to test our proposed method. This also mimics real-world data collection via crowdsourcing in the sense that certain user behavior is missing from the training data.

modified dialog bAbI tasks data
-----------------------------------------------------------------------
In this directory, there are 4 files -
modified-dialog-babi-task5-full-dialogs-dev.txt
modified-dialog-babi-task5-full-dialogs-trn.txt
modified-dialog-babi-task5-full-dialogs-tst-OOV.txt
modified-dialog-babi-task5-full-dialogs-tst.txt

The training and validation data has been modified, while the test and test-OOV sets are used from the original dialog bAbI tasks.
The specific changes to training and validation data, along with an example are described in detail in our paper.

Data format
==========================================
The file format for each task is similar to original bAbI dialog tasks:
a) The IDs for a given  dialog start at 1 and increase. When the IDs in a file reset back to 1 you can consider the following sentences as a new dialog.
b) When the bot speaks two times in a row, we used the special token "<SILENCE>" to fill in for the missing user utterance.

The goal is to predict the bot utterances, that can be sentences or API calls (sentences starting with the special token "api_call").

License
==========================================
This dataset is released under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.
A copy of this license is included with the data. You can also access the license at <http://creativecommons.org/licenses/by-nc-sa/4.0/>.

Contact
==========================================
For more details on the dataset and baselines, see the paper "Learning End-to-End Goal-Oriented Dialog with maximal User task success and minimal Human Agent use" by Janarthanan Rajendran, Jatin Ganhotra and Lazaros Polymenakos (arxiv link coming soon).

For any information, contact Jatin Ganhotra : jatinganhotra (at) us (dot) ibm (dot) com .