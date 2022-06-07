# ComMU


_arxiv link, github code link, dataset download link_


<iframe width="800" height="457" src="https://www.youtube.com/embed/yXFlF9nlB8Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>    

ComMU is a dataset for combinatorial music generation, a branch of conditional music generation. The dataset contains 12,025 MIDI samples written and created by professional composers, and is consisted of short note sequences of 4, 8, or 16 bars. MIDI files of the dataset are organized into 12 different metadata. Here are the following metadata and more information on the dataset:
BPM, Genre, Key, Track-instrument, Track-role, Time signature, Pitch range, Number of Measures, Chord progression, Min Velocity, Max Velocity, Rhythm



## Example of the Dataset

_2 sample clips go here_



## Pipeline of data collection

<div align="center">
  <img src="./assets/img/data_pipeline.png" width=1000x>
</div>


## Data Analysis

The distribution in note density and note length, according to track-role, is illustrated below. The shapes of the corresponding notes are dependent on track-role

<div align="center">
  <img src="./assets/img/figure_3.png" width=1000x>
</div>

While melody and accompaniment have short note lengths, bass and pad have longer notes. Note density shows that melody and accompaniment hold stronger, denser notes, whereas the bass and pad have a more weak but stable notes.




## Multi-track with Track-role

<div align="center">
  <img src="./assets/img/figure_7.png" width=1000x>
</div>

 - Figure above shows that with the introduction of track-role, a more appropriate music can be generated and can improve the capacity and flexibility of automatic composition.



<h3>Piano with 4 track-role</h3>

<table class="audio-table">
  <tbody>
    <tr>
      <td>Main Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_mainmelody/piano_mainmelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_mainmelody/piano_mainmelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_mainmelody/piano_mainmelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Sub Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_submelody/piano_submelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_submelody/piano_submelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_submelody/piano_submelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Accompaniment</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_accompaniment/piano_accompaniment_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_accompaniment/piano_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_accompaniment/piano_accompaniment_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Riff</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_riff/piano_riff_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_riff/piano_riff_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_riff/piano_riff_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </foot>
</table>



<h3>String with 4 track-role</h3>

<table class="audio-table">
  <tbody>
    <tr>
      <td>Main Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_mainmelody/string_mainmelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_mainmelody/string_mainmelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_mainmelody/string_mainmelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Sub Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_submmelody/string_submelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_submelody/string_submelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_submelody/string_submelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Accompaniment</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_accompaniment/string_accompaniment_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_accompaniment/string_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_accompaniment/string_accompaniment_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Riff</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_riff/string_riff_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_riff/string_riff_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_riff/string_riff_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </foot>
</table>


## Understanding the Task of CombinatorialMusic Generation
<div align="center">
  <img src="./assets/img/figure_1.png" width=1000x>
</div>
As shown above, the process of combinatorial music generation is divided into two stages. In stage 1, a note sequence is generated from a set of metadata. In stage 2, those note sequences are combined to produce a complete piece of music. Hence ComMU is utilized to tackle its task in stage 1.


## Listening sample music

randomly chosen metadata output. All music samples are generated.

_list samples with metadata_

<h3>Stage 1</h3>

<table class="audio-table">
  <tbody>
    <tr>
      <td>5 sample audio</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
</table>


## Listening music after combinatorial music generation stage1 and 2

All music samples are generated. stage2 is done by composers.

_list samples with metadata_


<h3>Stage 2</h3>

<table class="audio-table">
  <tbody>
    <tr>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/newage_trackrole/newage_inspiring.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
</table>




