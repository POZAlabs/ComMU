# ComMU

- <a href="https://github.com/POZAlabs/ComMU-code">Paper on arxiv(not yet available)</a>
- <a href="https://github.com/POZAlabs/ComMU-code">Code on github</a>
- <a href="./assets/ComMU.tar" download="ComMU.tar">Dataset download</a>
 

<iframe width="800" height="457" src="https://www.youtube.com/embed/yXFlF9nlB8Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>    
ComMU has 11,144 MIDI samples that consist of short note sequences created by professional composers with their corresponding 12 metadata. We propose combinatorial music generation, a new task that generate diverse and high-quality music only with metadata through auto-regressive language model. Here are the ComMU's 12 metadata:
- BPM, genre, key, instrument, track-role, time signature, pitch range, number of measures, chord progression, min velocity, max velocity, and rhythm.

# Example of the dataset

- <span style="color: #808080">bpm</span>: 100, #key: C major, #time_signature: 4/4 #number_of_measures: 8, #genre: cinematic, #rhythm: standard #track-role: accompaniment, #pitch_range: mid_low, #instruments: piano, #min_velocity: 36, #max_velocity: 40
#chord_progression: F - C - Am - G
<audio controls style="width: 400px;">
  <source src="./assets/example_data/1.wav" type="audio/mpeg">
</audio>

- #bpm: 120, #key: A minor, #time_signature: 3/4 #number_of_measures: 16, #genre: cinematic, #rhythm: standard #track-role: main_melody, #pitch_range: mid_high, #instruments: string, #min_velocity: 70, #max_velocity: 70
#chord_progression: Am - Em7 - FM7 - Em7 - Dm7 - CM7 - Bm7(b5) - E7 - Am - Em7 - FM7 - Em7 - Dm7 - CM7 - Bm7(b5) - E1 - Am
<audio controls style="width: 400px;">
  <source src="./assets/example_data/2.wav" type="audio/mpeg">
</audio>



# Pipeline of data collection

<div align="center">
  <img src="./assets/img/data_pipeline_3.png" width=1000x>
</div>



# Combinatorial music generation
<div align="center">
  <img src="./assets/img/figure_1.png" width=1000x>
</div>
As shown above, the process of combinatorial music generation is divided into two stages. In stage 1, a note sequence is generated from a set of metadata. In stage 2, those note sequences are combined to produce a complete piece of music. ComMU is utilized to solve stage 1.




## Stage 1
Audio samples are automatically generated only with descripted metadata.
 - Common metadata underlying the 5 clips are as follows:
      -  #bpm: 130, #key: A minor, #time_signature: 4/4
      -  #number_of_measures: 8, #genre: new age, #rhythm: standard
      -  #chord_progression: Am → F → C → G → A m → F → C → G  

 - #track-role: accompaniment, #pitch_range: mid_low, #instrument: piano, #min_velocity: 40, #max_velocity: 50
<audio controls style="width: 400px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_accompaniment_1.mp3" type="audio/mpeg">
</audio>

   - #track-role: main_melody, #pitch_range: mid, #instrument: piano, #min_velocity: 60, #max_velocity: 70
<audio controls style="width: 400px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_mainmelody_1.mp3" type="audio/mpeg">
</audio>

   - #track-role: pad, #pitch_range: mid_low, #instrument: piano, #min_velocity: 70, #max_velocity: 80
<audio controls style="width: 400px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_pad_piano_1.mp3" type="audio/mpeg">
</audio>

   - #track-role: pad, #pitch_range: mid_low, #instrument: string, #min_velocity: 2, #max_velocity: 127
<audio controls style="width: 400px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_pad_string_1.mp3" type="audio/mpeg">
</audio>

   - #track-role: riff, #pitch_range: mid_high, #instrument: piano, #min_velocity: 70, #max_velocity: 80
<audio controls style="width: 400px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_riff_1.mp3" type="audio/mpeg">
</audio>



## Stage 2
A human composer combines the 5 above audio samples, putting only 3-4 minutes to create the full song below.

<audio controls style="width: 600px;">
  <source src="./assets/audio_samples/track_role/newage_trackrole/newage_inspiring.mp3" type="audio/mpeg">
</audio>


# Ground truth vs. Generated
Our system does not reconstruct ground-truth samples but generate samples that have originality.
<table class="audio-table">
  <tbody>
    <tr>
      <td>Ground truth</td>
      <td>Generated</td>
    </tr>
    <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/1.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/1.wav" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/2.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/2.wav" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/3.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/3.wav" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/4.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/4.wav" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/5.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/5.wav" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
  <tfoot>
   <tr>
      <td><audio controls=""><source src="./assets/comparing/ground_truth/6.wav" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/comparing/generated/6.wav" type="audio/mpeg" /></audio></td>
    </tr>
  </tfoot>
</table>




# Multi-track with Track-role

<div align="center">
  <img src="./assets/img/figure_7.png" width=1000x>
</div>

Figure shows that the track-role can provides precise guidance to generated music.



<h3>Piano with 4 track-role</h3>
All metadata are the same except for track-role

<table class="audio-table">
  <tbody>
    <tr>
      <td>Main Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_mainmelody/piano_mainmelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_mainmelody/piano_mainmelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Sub Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_submelody/piano_submelody_000.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_submelody/piano_submelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Accompaniment</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_accompaniment/piano_accompaniment_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_accompaniment/piano_accompaniment_003.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Riff</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_riff/piano_riff_002.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/piano/piano_riff/piano_riff_003.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tfoot>
</table>



<h3>String with 4 track-role</h3>
All metadata are the same except for track-role

<table class="audio-table">
  <tbody>
    <tr>
      <td>Main Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_mainmelody/string_mainmelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_mainmelody/string_mainmelody_003.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Sub Melody</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_submelody/string_submelody_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_submelody/string_submelody_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
    <tr>
      <td>Accompaniment</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_accompaniment/string_accompaniment_002.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_accompaniment/string_accompaniment_003.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Riff</td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_riff/string_riff_001.mp3" type="audio/mpeg" /></audio></td>
      <td><audio controls=""><source src="./assets/audio_samples/track_role/string/string_riff/string_riff_002.mp3" type="audio/mpeg" /></audio></td>
    </tr>
  </tfoot>
</table>



