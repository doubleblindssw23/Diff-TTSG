# Diff-TTSG : Denoising probabilistic integrated speech and gesture synthesis


We present Diff-TTSG, the first diffusion model that jointly learns to synthesise speech and gestures together. Our method is non-autoregressive in nature and can be trained on small datasets from scratch. In addition, to showcase the efficacy of these systems and pave the way for their evaluation, we describe an improved set of uni- and multi-modal subjective tests for evaluating integrated speech and gesture synthesis systems.


<style type="text/css">
    .tg {
    border-collapse: collapse;
    border-color: #9ABAD9;
    border-spacing: 0;
  }

  .tg td {
    background-color: #EBF5FF;
    border-color: #9ABAD9;
    border-style: solid;
    border-width: 1px;
    color: #444;
    font-family: Arial, sans-serif;
    font-size: 14px;
    overflow: hidden;
    padding: 0px 20px;
    word-break: normal;
    font-weight: bold;
    vertical-align: middle;
    horizontal-align: center;
    white-space: nowrap;
  }

  .tg th {
    background-color: #000000;
    border-color: #9ABAD9;
    border-style: solid;
    border-width: 1px;
    color: #fff;
    font-family: Arial, sans-serif;
    font-size: 14px;
    font-weight: normal;
    overflow: hidden;
    padding: 0px 20px;
    word-break: normal;
    font-weight: bold;
    vertical-align: middle;
    horizontal-align: center;
    white-space: nowrap;
    padding: 10px;
    margin: auto;
  }

  .tg .tg-0pky {
    border-color: inherit;
    text-align: center;
    vertical-align: top,
  }

  .tg .tg-fymr {
    border-color: inherit;
    font-weight: bold;
    text-align: center;
    vertical-align: top
  }
  .slider {
  -webkit-appearance: none;
  width: 75%;
  height: 15px;
  border-radius: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: .2s;
  transition: opacity .2s;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: #409cff;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background: #409cff;
  cursor: pointer;
}

audio {
    width: 240px;
}

/* CSS */
.button-12 {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 6px 14px;
  font-family: -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
  border-radius: 6px;
  border: none;

  background: #6E6D70;
  box-shadow: 0px 0.5px 1px rgba(0, 0, 0, 0.1), inset 0px 0.5px 0.5px rgba(255, 255, 255, 0.5), 0px 0px 0px 0.5px rgba(0, 0, 0, 0.12);
  color: #DFDEDF;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-12:focus {
  box-shadow: inset 0px 0.8px 0px -0.25px rgba(255, 255, 255, 0.2), 0px 0.5px 1px rgba(0, 0, 0, 0.1), 0px 0px 0px 3.5px rgba(58, 108, 217, 0.5);
  outline: 0;
}

video {
  margin: 1em;
}


</style>


## Stimuli from the evaluation test

### Speech only evaluation


> "You walk around Dublin city centre and even if you try and strike up a conversation with somebody it's impossible because everyone has their headphones in. And again, I would listen to podcasts sometimes with my headphones in walking around the streets."
<table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">NAT</th>
      <th class="tg-0pky">Diff-TTSG</th>
      <th class="tg-0pky">T2-ISG</th>
      <th class="tg-0pky">Grad-TTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/GT_1_C4_2_eval_0137.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/TTSG_1_C4_2_eval_0137.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/ISG_1_C4_2_eval_0137.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/Grad-TTS_1_C4_2_eval_0137.wav" type="audio/wav">
          </audio>
        </td>
    </tr>
  </tbody>
</table>

> "And then a few weeks later after that my parents were away my granny was minding us and again I don't know why I told my brother to do this but I was like here."
<table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">NAT</th>
      <th class="tg-0pky">Diff-TTSG</th>
      <th class="tg-0pky">T2-ISG</th>
      <th class="tg-0pky">Grad-TTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/GT_2_C3_7_eval_0163.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/TTSG_2_C3_7_eval_0163.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/ISG_2_C3_7_eval_0163.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/Grad-TTS_2_C3_7_eval_0163.wav" type="audio/wav">
          </audio>
        </td>
    </tr>
  </tbody>
</table>

> "But I remember once my parents were just downstairs in the kitchen and this is when mobile phones just began coming out. So, like my oldest brother and my oldest sister had a mobile phone each I'm pretty sure."
<table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">NAT</th>
      <th class="tg-0pky">Diff-TTSG</th>
      <th class="tg-0pky">T2-ISG</th>
      <th class="tg-0pky">Grad-TTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/GT_3_C3_7_eval_0047.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/TTSG_3_C3_7_eval_0047.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/ISG_3_C3_7_eval_0047.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/Grad-TTS_3_C3_7_eval_0047.wav" type="audio/wav">
          </audio>
        </td>
    </tr>
  </tbody>
</table>

> "Eventually got to a point where I was like okay I need to stop doing this sort of stuff Like it just doesn't make any sense as to why because I was getting hurt like there was times where like, I was like tearing muscles and I never broke a bone which I'm pretty proud of."
<table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">NAT</th>
      <th class="tg-0pky">Diff-TTSG</th>
      <th class="tg-0pky">T2-ISG</th>
      <th class="tg-0pky">Grad-TTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/GT_4_C3_7_eval_0301.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/TTSG_4_C3_7_eval_0301.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/ISG_4_C3_7_eval_0301.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/Grad-TTS_4_C3_7_eval_0301.wav" type="audio/wav">
          </audio>
        </td>
    </tr>
  </tbody>
</table>
<!-- 
> "I would like replenish stock I would bring up stock for the off-license that sort of stuff So I was doing all the kind of the menial kind of jobs like the kind of boring tedious work that someone had to do."
<table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">NAT</th>
      <th class="tg-0pky">Diff-TTSG</th>
      <th class="tg-0pky">T2-ISG</th>
      <th class="tg-0pky">Grad-TTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/GT_5_C4_1_eval_0251.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/TTSG_5_C4_1_eval_0251.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/ISG_5_C4_1_eval_0251.wav" type="audio/wav">
          </audio>
        </td>
        <td class="tg-0pky">
          <audio id="audio-small" controls>
            <source src="./stimuli/audio-only/Grad-TTS_5_C4_1_eval_0251.wav" type="audio/wav">
          </audio>
        </td>
    </tr>
  </tbody>
</table> -->


### Gesture-only evaluation (no audio)

<video id="gesture-only-video" class="video-js" controls width="640" height="360">
    <source id="gesture-only-video-source" src="./stimuli/gesture-only/TTSG_1_C3_7_eval_0447.mp4" type='video/mp4' />
</video>

Currently loaded: <span id="playing-gesture-only" style="font-weight: bold;" > Diff-TTSG 1</span>

<script>
gesture_only_video = document.getElementById('gesture-only-video')
gesture_only_video_source = document.getElementById('gesture-only-video-source')
gesture_only_span_text =  document.getElementById('playing-gesture-only')
function play_video(filename, text){
    gesture_only_video.pause();
    gesture_only_video_source.src = filename;
    gesture_only_span_text.innerHTML = text;
    gesture_only_video.load();
    gesture_only_video.play();
}
</script>

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">#</th>
    <th class="tg-0pky">NAT</th>
    <th class="tg-0pky">Diff-TTSG</th>
    <th class="tg-0pky">T2-ISG</th>
    <th class="tg-0pky">[Grad-TTS]+M</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>1</td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/GT_1_C3_7_eval_0447.mp4', 'NAT 1')" >NAT 1</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/TTSG_1_C3_7_eval_0447.mp4', 'Diff-TTSG 1')" >Diff-TTSG 1</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/ISG_1_C3_7_eval_0447.mp4', 'T2-ISG 1')" >T2-ISG 1</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/Grad_1_C3_7_eval_0447.mp4', 'Grad-TTS + M 1')" >Grad-TTS + M 1</button></td>
  </tr>
  <tr>
    <td>2</td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/GT_2_C3_5_eval_0043.mp4', 'NAT 2')" >NAT 2</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/TTSG_2_C3_5_eval_0043.mp4', 'Diff-TTSG 2')" >Diff-TTSG 2</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/ISG_2_C3_5_eval_0043.mp4', 'T2-ISG 2')" >T2-ISG 2</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/Grad_2_C3_5_eval_0043.mp4', 'Grad-TTS + M 2')" >Grad-TTS + M 2</button></td>
  </tr>
  <tr>
    <td>3</td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/GT_3_C4_2_eval_0039.mp4', 'NAT 3')" >NAT 3</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/TTSG_3_C4_2_eval_0039.mp4', 'Diff-TTSG 3')" >Diff-TTSG 3</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/ISG_3_C4_2_eval_0039.mp4', 'T2-ISG 3')" >T2-ISG 3</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/Grad_3_C4_2_eval_0039.mp4', 'Grad-TTS + M 3')" >Grad-TTS + M 3</button></td>
  </tr>
  <tr>
    <td>4</td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/GT_4_C4_3_eval_0092.mp4', 'NAT 4')" >NAT 4</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/TTSG_4_C4_3_eval_0092.mp4', 'Diff-TTSG 4')" >Diff-TTSG 4</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/ISG_4_C4_3_eval_0092.mp4', 'T2-ISG 4')" >T2-ISG 4</button></td>
    <td><button class="button-12" role="button" onclick="play_video('stimuli/gesture-only/Grad_4_C4_3_eval_0092.mp4', 'Grad-TTS + M 4')" >Grad-TTS + M 4</button></td>
  </tr>
</tbody>
</table>


### Speech-and-gesture evaluation



<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Matched</th>
    <th class="tg-0pky">Mismatched</th>
  </tr>
</thead>
<tbody>
  <tr>
      <td> 
          <video id="speech-and-gesture-video-matched" class="video-js" controls width="500" height="282">
              <source id="speech-and-gesture-video-matched-source" src="./stimuli/speech-and-gesture/TTSG_C4_3_eval_0150_matched.mp4" type='video/mp4' />
          </video>
      </td>
      <td>
        <video id="speech-and-gesture-video-mismatched" class="video-js" controls width="500" height="282">
              <source id="speech-and-gesture-video-mismatched-source" src="./stimuli/speech-and-gesture/TTSG_C4_3_eval_0150_mismatched.mp4" type='video/mp4' />
          </video>
      </td>
  </tr>
</tbody>
</table>


Currently loaded: <span id="playing-speech-and-gesture-span" style="font-weight: bold;" > Diff-TTSG 1</span>




<script>
speech_and_gesture_video_matched = document.getElementById('speech-and-gesture-video-matched')
speech_and_gesture_video_matched_source = document.getElementById('speech-and-gesture-video-matched-source')

speech_ang_gesture_video_mismatched = document.getElementById('speech-and-gesture-video-mismatched')
speech_and_gesture_video_mismatched_source = document.getElementById('speech-and-gesture-video-mismatched-source')

speech_and_gesture_span_text =  document.getElementById('playing-speech-and-gesture-span')
function play_speech_and_gesture_eval(matched_filename, mismatched_filename, text){
    speech_and_gesture_video_matched.pause();
    speech_ang_gesture_video_mismatched.pause();

    speech_and_gesture_video_matched_source.src = matched_filename;
    speech_and_gesture_video_mismatched_source.src = mismatched_filename;

    speech_and_gesture_span_text.innerHTML = text;

    speech_and_gesture_video_matched.load();
    speech_ang_gesture_video_mismatched.load();
}
</script>




<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">#</th>
    <th class="tg-0pky">NAT</th>
    <th class="tg-0pky">Diff-TTSG</th>
    <th class="tg-0pky">T2-ISG</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>1</td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/GT_C4_3_eval_0150_matched.mp4', './stimuli/speech-and-gesture/GT_C4_3_eval_0150_mismatched.mp4' ,'NAT 1')" >NAT 1</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/TTSG_C4_3_eval_0150_matched.mp4', './stimuli/speech-and-gesture/TTSG_C4_3_eval_0150_mismatched.mp4' ,'Diff-TTSG 1')" >Diff-TTSG 1</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/ISG_C4_3_eval_0150_matched.mp4', './stimuli/speech-and-gesture/ISG_C4_3_eval_0150_mismatched.mp4' ,'T2-ISG 1')" >T2-ISG 1</button></td>
  </tr>
  <tr>
    <td>2</td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/GT_C3_7_eval_1074_matched.mp4', './stimuli/speech-and-gesture/GT_C3_7_eval_1074_mismatched.mp4' ,'NAT 2')" >NAT 2</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/TTSG_C3_7_eval_1074_matched.mp4', './stimuli/speech-and-gesture/TTSG_C3_7_eval_1074_mismatched.mp4' ,'Diff-TTSG 2')" >Diff-TTSG 2</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/ISG_C3_7_eval_1074_matched.mp4', './stimuli/speech-and-gesture/ISG_C3_7_eval_1074_mismatched.mp4' ,'T2-ISG 2')" >T2-ISG 2</button></td>
  </tr>
  <tr>
    <td>3</td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/GT_C4_2_eval_0137_matched.mp4', './stimuli/speech-and-gesture/GT_C4_2_eval_0137_mismatched.mp4' ,'NAT 3')" >NAT 3</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/TTSG_C4_2_eval_0137_matched.mp4.mp4', './stimuli/speech-and-gesture/TTSG_C4_2_eval_0137_mismatched.mp4' ,'Diff-TTSG 3')" >Diff-TTSG 3</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/ISG_C4_2_eval_0137_matched.mp4', './stimuli/speech-and-gesture/ISG_C4_2_eval_0137_mismatched.mp4' ,'T2-ISG 3')" >T2-ISG 3</button></td>
  </tr>
  <tr>
    <td>4</td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/GT_C4_2_eval_0011_matched.mp4', './stimuli/speech-and-gesture/GT_C4_2_eval_0011_mismatched.mp4' ,'NAT 4')" >NAT 4</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/TTSG_C4_2_eval_0011_matched.mp4', './stimuli/speech-and-gesture/TTSG_C4_2_eval_0011_mismatched.mp4' ,'Diff-TTSG 4')" >Diff-TTSG 4</button></td>
    <td><button class="button-12" role="button" onclick="play_speech_and_gesture_eval('./stimuli/speech-and-gesture/ISG_C4_2_eval_0011_matched.mp4', './stimuli/speech-and-gesture/ISG_C4_2_eval_0011_mismatched.mp4' ,'T2-ISG 4')" >T2-ISG 4</button></td>
  </tr>
</tbody>
</table>


