## Overview

This directory contains modified-bAbI dialog tasks, an extension of original-bAbI dialog tasks, as described in the paper:   
**Learning End-to-End Goal-Oriented Dialog with maximal User task success and minimal Human Agent use**   
Janarthanan Rajendran, Jatin Ganhotra and Lazaros Polymenakos  
[https://www.aclweb.org/anthology/Q19-1024/](https://www.aclweb.org/anthology/Q19-1024/)  
accepted at [TACL](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00274) and oral presentation at ACL 2019 - [https://vimeo.com/384015139](https://vimeo.com/384015139).


Neural end-to-end goal-oriented dialog systems showed promise to reduce the workload of human agents for customer service, as well as reduce wait time for users. However, their inability to handle new user behavior at deployment has limited their usage in real world.

In this work, we propose an end-to-end trainable method for neural goal-oriented dialog systems which handles new user behaviors at deployment by transferring the dialog to a human agent intelligently. The proposed method has three goals: 

1. maximize user's task success by transferring to human agents, 
2. minimize the load on the human agents by transferring to them only when it is essential, and 
3. learn online from the human agent's responses to reduce human agents load further. 

We evaluate our proposed method on a modified-bAbI dialog task that simulates the scenario of new user behaviors occurring at test time. Experimental results show that our proposed method is effective in achieving the desired goals.

We modify the original-bAbI dialog tasks, by removing and replacing certain user behaviors from the training and validation data. The test set is left untouched. This simulates a scenario where some new user behaviors arise during the test (deployment) time that were not seen during the training and hence allows us to test our proposed method. This also mimics real-world data collection via crowdsourcing in the sense that certain user behavior is missing from the training data.

## Modified bAbI dialog tasks

Adaptation of the "Dialog bAbI tasks data" dataset released by Facebook, available at https://research.fb.com/downloads/babi/, under the CC BY 3.0 Unported license, available at https://creativecommons.org/licenses/by/3.0/legalcode.

In this directory, there are 4 files -

- modified-dialog-babi-task5-full-dialogs-dev.txt
- modified-dialog-babi-task5-full-dialogs-trn.txt
- modified-dialog-babi-task5-full-dialogs-tst-OOV.txt
- modified-dialog-babi-task5-full-dialogs-tst.txt

The training and validation data has been modified, while the test and test-OOV sets are used from the original dialog bAbI tasks.
The specific changes to training and validation data, along with an example are described in detail in our paper.

### Data format

The file format for each task is similar to original bAbI dialog tasks:  

- The IDs for a given  dialog start at 1 and increase. When the IDs in a file reset back to 1 you can consider the following sentences as a new dialog.
- When the bot speaks two times in a row, we used the special token "<SILENCE>" to fill in for the missing user utterance.

The goal is to predict the bot utterances, that can be sentences or API calls (sentences starting with the special token `api_call`).

## License

The dataset is released under [**CC BY-SA
4.0**](https://creativecommons.org/licenses/by-sa/4.0/) license. For the full
license, see [LICENSE.txt](LICENSE.txt). Please cite the following paper if you
use this dataset in your work

```text
@article{rajendran-etal-2019-learning,
    title = "Learning End-to-End Goal-Oriented Dialog with Maximal User Task Success and Minimal Human Agent Use",
    author = "Rajendran, Janarthanan  and
      Ganhotra, Jatin  and
      Polymenakos, Lazaros C.",
    journal = "Transactions of the Association for Computational Linguistics",
    volume = "7",
    month = mar,
    year = "2019",
    url = "https://www.aclweb.org/anthology/Q19-1024",
    doi = "10.1162/tacl_a_00274",
    pages = "375--386",
    abstract = "Neural end-to-end goal-oriented dialog systems showed promise to reduce the workload of human agents for customer service, as well as reduce wait time for users. However, their inability to handle new user behavior at deployment has limited their usage in real world. In this work, we propose an end-to-end trainable method for neural goal-oriented dialog systems that handles new user behaviors at deployment by transferring the dialog to a human agent intelligently. The proposed method has three goals: 1) maximize user's task success by transferring to human agents, 2) minimize the load on the human agents by transferring to them only when it is essential, and 3) learn online from the human agent's responses to reduce human agents' load further. We evaluate our proposed method on a modified-bAbI dialog task, which simulates the scenario of new user behaviors occurring at test time. Experimental results show that our proposed method is effective in achieving the desired goals.",
}
```


## Dataset Metadata
The following table is necessary for this dataset to be indexed by search
engines such as <a href="https://g.co/datasetsearch">Google Dataset Search</a>.
<div itemscope itemtype="http://schema.org/Dataset">
<table>
  <tr>
    <th>property</th>
    <th>value</th>
  </tr>
  <tr>
    <td>name</td>
    <td><code itemprop="name">Modified bAbI dialog task </code></td>
  </tr>
  <tr>
    <td>alternateName</td>
    <td><code itemprop="alternateName">modified-bAbI-dialog-tasks</code></td>
  </tr>
  <tr>
    <td>url</td>
    <td><code itemprop="url">https://github.com/IBM/modified-bAbI-dialog-tasks</code></td>
  </tr>
  <tr>
    <td>sameAs</td>
    <td><code itemprop="sameAs">https://github.com/IBM/modified-bAbI-dialog-tasks</code></td>
  </tr>
  <tr>
    <td>description</td>
    <td><code itemprop="description"></code></td>
  </tr>
  <tr>
    <td>provider</td>
    <td>
      <div itemscope itemtype="http://schema.org/Organization" itemprop="provider">
        <table>
          <tr>
            <th>property</th>
            <th>value</th>
          </tr>
          <tr>
            <td>name</td>
            <td><code itemprop="name">IBM</code></td>
          </tr>
          <tr>
            <td>sameAs</td>
            <td><code itemprop="sameAs">https://en.wikipedia.org/wiki/IBM</code></td>
          </tr>
        </table>
      </div>
    </td>
  </tr>
  <tr>
    <td>citation</td>
    <td><code itemprop="citation">https://www.aclweb.org/anthology/Q19-1024/</code></td>
  </tr>
</table>
</div>

## Contact

For more details on the dataset and baselines, see the paper:  
 
**Learning End-to-End Goal-Oriented Dialog with maximal User task success and minimal Human Agent use**   
Janarthanan Rajendran, Jatin Ganhotra and Lazaros Polymenakos  
[https://www.aclweb.org/anthology/Q19-1024/](https://www.aclweb.org/anthology/Q19-1024/)  
accepted at [TACL](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00274) and oral presentation at ACL 2019 - [https://vimeo.com/384015139](https://vimeo.com/384015139).

For any information, contact Jatin Ganhotra : jatinganhotra (at) us (dot) ibm (dot) com 
