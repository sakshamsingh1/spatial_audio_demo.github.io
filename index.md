---
layout: default
---

<br>

## Abstract
Spatial audio is a crucial component in creating immersive experiences. However, recording it precisely can require expensive and specialized setups. Traditional simulation-based approaches to generate spatial audio rely on expertise, have limited scalability, and assume independence between semantic and spatial information. To address these issues, we explore end-to-end spatial audio generation. We introduce and formulate a new task of generating first-order Ambisonics given a sound category and sound source spatial location. We propose Diff-SAGe, an end-to-end flow-matching transformer diffusion model to approach this task. We carry out comprehensive evaluations on objective metrics related to input conditioning and generation metrics. Through extensive comparisons on two datasets, we show our end-to-end method outperforms the traditional baselines on both quantitative and qualitative metrics. 

<p>
    <img src="public/images/task.pdf" width="50%" class="center" alt>
</p>


<iframe width="70%" class="center" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/J-pBzCMyUKE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Examples for TAU-NIGENS Spatial Sound Events 2020 (TAU-NIGENS-20) dataset

Randomly selected examples.

<div style="display:flex; justify-content:center;">
<table style="display:flex; justify-content:safe center; overflow:scroll;" text-align='center'>
    <tr>
        <th></th>
        <th>Ground-Truth</th>
        <th>Diff-SAGe (Ours)</th>
        <th>Reference Audio (Simulated)</th>
        <th>Tango (Simulated)</th>
        <th>AudioLDM (Simulated)</th>
    </tr>
    <tr>
        <td>Alarm</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/alarm.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/alarm.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/alarm.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/alarm.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/alarm.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Baby Crying</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/baby_crying.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/baby_crying.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/baby_crying.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/baby_crying.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/baby_crying.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Crash</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/cash.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/cash.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/cash.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/cash.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/cash.wav" controls></audio></td>
    </tr>    
    <tr>
        <td>Dog Barking</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/dog_barking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/dog_barking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/dog_barking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/dog_barking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/dog_barking.wav" controls></audio></td>
    </tr>    
    <tr>
        <td>Enging running</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/engine_running.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/engine_running.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/engine_running.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/engine_running.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/engine_running.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Female Screaming</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/female_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/female_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/female_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/female_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/female_screaming.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Female Speaking</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/female_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/female_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/female_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/female_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/female_speaking.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Fire Burning</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/fire_burning.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/fire_burning.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/fire_burning.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/fire_burning.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/fire_burning.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Footsteps</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/footsteps.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/footsteps.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/footsteps.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/footsteps.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/footsteps.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Door Knock</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/knocking_on_door.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/knocking_on_door.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/knocking_on_door.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/knocking_on_door.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/knocking_on_door.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Male Screaming</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/male_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/male_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/male_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/male_screaming.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/male_screaming.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Male speaking</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/male_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/male_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/male_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/male_speaking.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/male_speaking.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Phone ringing</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/phone_ringing.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/phone_ringing.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/phone_ringing.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/phone_ringing.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/phone_ringing.wav" controls></audio></td>
    </tr>
    <tr>
        <td>Piano</td>
        <td><audio src="public/audios/dcase20/dcase20_eval/piano.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_L/piano.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_origAudio/piano.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_audioLDM/piano.wav" controls></audio></td>
        <td><audio src="public/audios/dcase20/dcase20_tango/piano.wav" controls></audio></td>
    </tr>
</table>
</div>

<br>

