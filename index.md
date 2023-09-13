---
layout: default
---

<br>

# User Input Condition

Creating Foley sounds manually is challenging and labor-intensive work. Therefore, the ultimate goal of this study is automating the Foley sound synthesis to allow anyone to easily generate sounds. 
However, in real-world applications, directly inputting event timing features, such as power and RMS, is not straightforward for users. In this manner, receiving the audio that can serve as a reference of event timings and extracting its event timing features to use as sampling conditions would be more intuitive. 

To demonstrate that **T-Foley** performs well in such use cases, we conducted experiments using various types of sound(e.g. clapping, voice) as timing condition references. We manually recorded target samples delivering the desired timing points and then these recorded sounds are used as event timing conditions to generate sounds in different categories.

## 1. Clap

When target sample, which indicate when the events should occur, is recorded by clapping.

<iframe width="80%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/3YiWd7MVEx0?si=Wz5knZIkMxbiRdtH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
<!-- <video width="80%" controls>
  <source src="public/videos/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video> -->

## 2. Voice

When target sample is recorded with human voices.

<div style="display:flex; justify-content:center;">
<table style="display:flex; overflow:scroll;" text-align='center'>
    <tr>
        <th>DogBark</th>
        <th>GunShot</th>
        <th>MovingMotorVehicle</th>
    </tr>
    <tr>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/UwQMfa64Rhg?si=g-cLvOpTAdnxN4Ho" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/kXHTmGZdw_A?si=Q2xk6vAUDSOP4Er0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/ww6g6gs5DEI?si=Hn3vQKigwmsxJzd4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
    </tr>
    <tr>
        <th>Keyboard</th>
        <th>Rain</th>
        <th>Footstep</th>
    </tr>
    <tr>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/m2oRJhoU97s?si=ZbTxoB1ZAMbDAaaE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/fd3cSH5-6A4?si=htLCJNAs3hT3BNlH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
        <td><iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/gyAHCiY6vCE?si=Rre4pNOeO24ZOV3Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></td>
    </tr>
</table>
</div>


The generated results demonstrated that our model has the ability to generate high-quality Foley sounds using even clapping sounds or human voicesas event timing features. Through this, we have confirmed the potential and practical applicability of this work.

<br>

---

# Temporal Event Conditioning Methods

Figure 1 and following demo samples contain the target samples, along with the corresponding 3 generated samples following each conditioning method. The first row is the sounds used to extract targeting event timing features. Subsequent rows are the generated results in different conditioning blocks (FiLM, TFiLM, and BFiLM). Columns for different sound categories (Gunshot, Footstep, and Keyboard)

<p>
    <img src="public/images/event-guided_samples.png" alt>
    <em text-align="center">Figure 1: Generated sound in Mel-spectrogram with conditioning target event timing feature. As shown in the spectrograms, it can be observed that FiLM exhibits the occurrence of unclear sounds that are not aligned with the timing of the target samples. In contrast, the other two methods demonstrate excellent synchronization of timing which means that temporal FiLM and block FiLM outperform the original method.</em>
</p>

<br>

<div style="display:flex; justify-content:center;">
<table style="display:flex; overflow:scroll;" text-align='center'>
    <tr>
        <th></th>
        <th>GunShot</th>
        <th>Footstep</th>
        <th>Sneeze/Cough</th>
    </tr>
    <tr>
        <td>Target</td>
        <td><audio src="public/audios/097_gunshot.wav" controls></audio></td>
        <td><audio src="public/audios/094_footstep.wav" controls></audio></td>
        <td><audio src="public/audios/014_sneeze_cough.wav" controls></audio></td>
    </tr>
    <tr>
        <td>FiLM</td>
        <td><audio src="public/audios/097_gunshot_Film.wav" controls></audio></td>
        <td><audio src="public/audios/094_footstep_Film.wav" controls></audio></td>
        <td><audio src="public/audios/014_sneeze_cough_Film.wav" controls></audio></td>
    </tr>
    <tr>
        <td>TFiLM</td>
        <td><audio src="public/audios/097_gunshot_TFilm.wav" controls></audio></td>
        <td><audio src="public/audios/094_footstep_TFilm.wav" controls></audio></td>
        <td><audio src="public/audios/014_sneeze_cough_TFilm.wav" controls></audio></td>
    </tr>
    <tr>
        <td>BFiLM</td>
        <td><audio src="public/audios/097_gunshot_BFilm.wav" controls></audio></td>
        <td><audio src="public/audios/094_footstep_BFilm.wav" controls></audio></td>
        <td><audio src="public/audios/014_sneeze_cough_BFilm.wav" controls></audio></td>
    </tr>
</table>
</div>

<br>

# Vocal conditions

While controllable foley sound synthesis holds immense potential, inputting event features directly into real-world applications can be challenging for users. Therefore, we propose using vocal audio mimicking foley sound as a reference for extracting temporal event conditions, offering ease and intuitiveness. To evaluate the performance in such scenarios, we assess T-Foley using subsets of two vocal datasets that mimic foley sounds: *VocalImitationSet* and *VocalSketch*. We release the corresponding subsets: <a href="public/VocalImitationSet_subset_foley.csv">VocalImitationSet</a> and <a href="public/VocalSketch_subset_foley.csv">VocalSketch</a>.

<div style="display:flex; justify-content:center;">
<table style="display:flex; overflow:scroll;" text-align='center'>
    <tr>
        <th></th>
        <th>Vocal Condition</th>
        <th>T-Foley</th>
        <th>Mixed (L:Vocal, R:T-Foley)</th>
    </tr>
    <tr>
        <td>DogBark</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/dog_bark/009.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/dog_bark/009.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/dog_bark/009_mix_to_R.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Footstep</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/footstep/013.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/footstep/013.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/footstep/013_mix_to_R.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Gunshot</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/gunshot/055.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/gunshot/055.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/gunshot/055_mix_to_R.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Keyboard</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/keyboard/002.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/keyboard/002.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/keyboard/002_mix_to_R.wav" controls></audio></td>
    </tr>
    <tr>
        <td>MovingMotorVehicle</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/moving_motor_vehicle/018.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/moving_motor_vehicle/018.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/moving_motor_vehicle/018_mix_to_R.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Rain</td>
        <td><audio src="public/audios/vocal_conditions/voice_input/rain/018.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/rain/018.wav" controls></audio></td>
        <td><audio src="public/audios/vocal_conditions/generated/rain/018_mix_to_R.wav" controls></audio></td>
    </tr>
</table>
</div>

<br>

# Why T-Foley?

Generating foley sounds using temporal event conditions produces significantly more realistic outcomes compared to manual foley sound manipulation. We illustrate two specific applications. Firstly, envision a situation involving consecutive machine gunshots. Manually adjusting and joining individual gunshot sound snippets can result in an unnatural audio sequence. Conversely, employing T-Foley to concatenate temporal event conditions leads to a seamless and lifelike sound. Secondly, contemplate two scenarios: typing vigorously on a typewriter and softly pressing keys on a plastic keyboard. T-Foley can generate these sounds using identical temporal event features while varying the overall amplitude. It is important to note that the temporal event feature encloses information regarding sound timing and intensity.

<p>
        <img src="public/images/control_samples.png" width="50%" align="center" alt> <br>
        <em text-align="center">Figure 2: (a) Comparing manually synthesized consecutive gunshot sounds with sounds generated through temporal event feature. (b) Generated sounds with the original temporal event features and those with features reduced by a factor of 10.</em>
</p>

<div style="display:flex; justify-content:center;">
<table style="display:inline-table; overflow:scroll;" text-align='center'>
    <tr>
        <td>Original</td>
        <td>Original</td>
    </tr>
    <tr>
        <td><audio src="public/audios/control_rms/gunshot_original.wav" controls></audio></td>
        <td><audio src="public/audios/control_rms/keyboard_original.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Concatenated</td>
        <td>Generated with<br>original RMS</td>
    </tr>
    <tr>
        <td><audio src="public/audios/control_rms/gunshot_high-sparsity_shifted.wav" controls></audio></td>
        <td><audio src="public/audios/control_rms/keyboard_original_rms.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Generated</td>
        <td>Generated with<br>/10 RMS</td>
    </tr>
    <tr>
        <td><audio src="public/audios/control_rms/gunshot_high-sparsity_generated.wav" controls></audio></td>
        <td><audio src="public/audios/control_rms/keyboard_reduced_rms.wav" controls></audio></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
    </tr>
</table>
</div>

