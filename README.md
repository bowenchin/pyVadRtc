# PyVadRtc

Python script for Voice Activity Detection using webrtcvad Python package. webrtcvad utilizes VAD that Google developed for the WebRTC project, which is reportedly one of the best available, being fast, modern and free.

## Getting Started
- Install the packages found in [`requirements.txt`](./requirements.txt)
- Uses WebRTC Voice Activity Detection from https://github.com/wiseman/py-webrtcvad

```bash
pip install webrtcvad
pip install pydub
```

## Usage

[`pyVadRtc.py`](./pyVadRtc.py)
```python
from pydub import AudioSegment
import webrtcvad

# gap_time: gap time from start of audio to when speech is first detected
print('Gap Time: %s' % gap_time)
# end_time: time in audio where speech ends
print('End Time: %s' % end_time)
# speech_duration: duration of speech within the audio
print('Speech Duration: %s' % speech_duration)
```

Run Script
```bash
python pyVadRtc.py <aggressiveness: 0-3> <path to wav file>
```