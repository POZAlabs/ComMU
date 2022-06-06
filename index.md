# ComMU


_arxiv link, github code link, dataset download link_


<iframe width="800" height="457" src="https://www.youtube.com/embed/yXFlF9nlB8Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>    

ComMU is a dataset for combinatorial music generation, a branch of conditional music generation. The dataset contains 12,025 MIDI samples written and created by professional composers, and is consisted of short note sequences of 4, 8, or 16 bars. MIDI files of the dataset are organized into 12 different metadata. Here are the following metadata and more information on the dataset:

1. BPM
2. Genre
3. Key
4. Track instrument
5. Track-role
6. Time signature
7. Pitch range
8. Number of Measures
9. Chord progression
10. Min Velocity
11. Max Velocity
12. Rhythm



## Example of the Dataset

_2 sample clips go here_




## Data Analysis

The distribution in note density and note length, according to track-role, is illustrated below. The shapes of the corresponding notes are dependent on track-role

<div align="center">
  <img src="./assets/img/figure_3.png" width=1000x>
</div>

While melody and accompaniment have short note lengths, bass and pad have longer notes. Note density shows that melody and accompaniment hold stronger, denser notes, whereas the bass and pad have a more weak but stable notes.


<div align="center">
  <img src="./assets/img/figure_4.png" width=1000x>
</div>

The metadata heat map above illustrates the correlation between instruments, track-role, and pitch range. The map suggests that when a music is generated without track-role information, a piece that is highly correlated with the track-role will be generated. Conversely, without track-role information, a piece with low correlation will most likely not be generated -- meaning lower diversity in the tracks created.


## Pipeline of data collection

figure: how to collection the data



## Extended Chord Quality

<div align="center">
  <img src="./assets/img/figure_6.png" width=1000x>
</div>

 - Figure above illustrates that ComMU not only has major, minor, diminished and augmented 7th but also has extended chord qualities such as suspended 4th, major 7th, and minor 7th.




## Multi-track with Track-role

<div align="center">
  <img src="./assets/img/figure_7.png" width=1000x>
</div>

 - Figure above shows that with the introduction of track-role, a more appropriate music can be generated and can improve the capacity and flexibility of automatic composition.

_comparing music with various track-role_



## Understanding the Task of Combinatorial Music Generation

<div align="center">
  <img src="./assets/img/figure_1.png" width=1000x>
</div>

As shown above, the process of combinatorial music generation is divided into two stages. In stage 1, a note sequence is generated from a set of metadata. In stage 2, those note sequences are combined to produce a complete piece of music. Hence ComMU is utilized to tackle its task in stage 1.




## Listening sample music

randomly chosen metadata output. All music samples are generated.

_list samples with metadata_



## Listening music after combinatorial music generation stage1 and 2

All music samples are generated. stage2 is done by composers.

_list samples with metadata_
