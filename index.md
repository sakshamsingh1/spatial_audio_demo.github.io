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
Randomly selected examples. (Some samples may have low volume, so you may need to increase the audio level.)

<div style="display: flex; justify-content: center;">
  <table style="width: 800px; table-layout: fixed; text-align: center; border-collapse: collapse;">
    <tr>
      <th style="width: 150px;"></th>
      <th style="width: 150px; white-space: normal;">Ground-Truth</th>
      <th style="width: 150px; white-space: normal;">Diff-SAGe<br>(Ours)</th>
      <th style="width: 150px; white-space: normal;">Reference Audio<br>(Simulated)</th>
      <th style="width: 150px; white-space: normal;">AudioLDM<br>(Simulated)</th>
      <th style="width: 150px; white-space: normal;">Tango<br>(Simulated)</th>
    </tr>
    <tr>
      <td>Alarm</td>
      <td><audio src="public/dcase20/dcase20_eval/alarm.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/alarm.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/alarm.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/alarm.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/alarm.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Baby Crying</td>
      <td><audio src="public/dcase20/dcase20_eval/baby_crying.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/baby_crying.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/baby_crying.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/baby_crying.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/baby_crying.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Crash</td>
      <td><audio src="public/dcase20/dcase20_eval/crash.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/crash.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/crash.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/crash.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/crash.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Dog Barking</td>
      <td><audio src="public/dcase20/dcase20_eval/dog_barking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/dog_barking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/dog_barking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/dog_barking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/dog_barking.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Engine Running</td>
      <td><audio src="public/dcase20/dcase20_eval/engine_running.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/engine_running.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/engine_running.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/engine_running.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/engine_running.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Female Screaming</td>
      <td><audio src="public/dcase20/dcase20_eval/female_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/female_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/female_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/female_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/female_screaming.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Female Speaking</td>
      <td><audio src="public/dcase20/dcase20_eval/female_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/female_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/female_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/female_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/female_speaking.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Fire Burning</td>
      <td><audio src="public/dcase20/dcase20_eval/fire_burning.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/fire_burning.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/fire_burning.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/fire_burning.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/fire_burning.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Footsteps</td>
      <td><audio src="public/dcase20/dcase20_eval/footsteps.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/footsteps.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/footsteps.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/footsteps.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/footsteps.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Door Knock</td>
      <td><audio src="public/dcase20/dcase20_eval/knocking_on_door.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/knocking_on_door.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/knocking_on_door.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/knocking_on_door.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/knocking_on_door.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Male Screaming</td>
      <td><audio src="public/dcase20/dcase20_eval/male_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/male_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/male_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/male_screaming.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/male_screaming.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Male Speaking</td>
      <td><audio src="public/dcase20/dcase20_eval/male_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/male_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/male_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/male_speaking.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/male_speaking.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Phone Ringing</td>
      <td><audio src="public/dcase20/dcase20_eval/phone_ringing.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/phone_ringing.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/phone_ringing.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/phone_ringing.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/phone_ringing.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Piano</td>
      <td><audio src="public/dcase20/dcase20_eval/piano.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_L/piano.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_origAudio/piano.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_audioldm/piano.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase20/dcase20_tango/piano.wav" controls style="width: 140px;"></audio></td>
    </tr>
  </table>
</div>

## Examples for TAU Spatial Sound Events 2019 (TAU-19) dataset
Randomly selected examples. (Some samples may have low volume, so you may need to increase the audio level.)

<div style="display: flex; justify-content: center;">
  <table style="width: 800px; table-layout: fixed; text-align: center; border-collapse: collapse;">
    <tr>
      <th style="width: 150px;"></th>
      <th style="width: 150px; white-space: normal;">Ground-Truth</th>
      <th style="width: 150px; white-space: normal;">Diff-SAGe<br>(Ours)</th>
      <th style="width: 150px; white-space: normal;">Reference Audio<br>(Simulated)</th>
      <th style="width: 150px; white-space: normal;">AudioLDM<br>(Simulated)</th>
      <th style="width: 150px; white-space: normal;">Tango<br>(Simulated)</th>
    </tr>
    <tr>
      <td>Clearthroat</td>
      <td><audio src="public/dcase19/dcase19_eval/clearthroat.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/clearthroat.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/clearthroat.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/clearthroat.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/clearthroat.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Cough</td>
      <td><audio src="public/dcase19/dcase19_eval/cough.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/cough.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/cough.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/cough.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/cough.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Door Slam</td>
      <td><audio src="public/dcase19/dcase19_eval/doorslam.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/doorslam.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/doorslam.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/doorslam.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/doorslam.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Drawer</td>
      <td><audio src="public/dcase19/dcase19_eval/drawer.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/drawer.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/drawer.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/drawer.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/drawer.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td><audio src="public/dcase19/dcase19_eval/keyboard.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/keyboard.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/keyboard.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/keyboard.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/keyboard.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Keys Drop</td>
      <td><audio src="public/dcase19/dcase19_eval/keysDrop.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/keysDrop.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/keysDrop.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/keysDrop.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/keysDrop.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Knock</td>
      <td><audio src="public/dcase19/dcase19_eval/knock.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/knock.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/knock.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/knock.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/knock.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Laughter</td>
      <td><audio src="public/dcase19/dcase19_eval/laughter.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/laughter.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/laughter.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/laughter.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/laughter.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Page Turn</td>
      <td><audio src="public/dcase19/dcase19_eval/pageturn.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/pageturn.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/pageturn.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/pageturn.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/pageturn.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Phone</td>
      <td><audio src="public/dcase19/dcase19_eval/phone.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/phone.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/phone.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/phone.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/phone.wav" controls style="width: 140px;"></audio></td>
    </tr>
    <tr>
      <td>Speech</td>
      <td><audio src="public/dcase19/dcase19_eval/speech.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_L/speech.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_origAudio/speech.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_audioldm/speech.wav" controls style="width: 140px;"></audio></td>
      <td><audio src="public/dcase19/dcase19_tango/speech.wav" controls style="width: 140px;"></audio></td>
    </tr>
  </table>
</div>
<br>
