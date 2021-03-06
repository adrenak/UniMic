## UniMic
A convenience wrapper for Unity's Microphone class.

## API
`Mic` class in the `Adrenak.UniMic` namespace is a singleton and is accessed using `Mic.Instance`


### Properties
- `IsRecording` 
Returns if the Mic instance is recording audio

- `Frequency`
The frequency of the Microphone AudioClip

- `Sample`
The last populated sample of the audio data

- `SampleDurationMS`
The duration of the sample segment in milliseconds that the instance maintains and fires in events. 

- `SampleLength`
The number of samples in the sample segment

- `AudioClip`
The inner `AudioClip` of the instance

- `Devices`
The recording devices that are connected to the machine running the code

- `CurrentDeviceIndex`
The index of the active device in the `Devices` list

- `CurrentDeviceName`
The name of the active device


### Events
- `OnStartRecording`
Event fired when the instance starts to record the audio

- `OnStopRecording`
Event fired when the instance stops recording the audio

- `OnSampleReady`
Event fired when a sample of `SampleLength` has been populated by the instance

### Methods
- `UpdateDevices` updates the list of available recording devices. 

- `ChangeDevice` changes the recording device. The method internally restarts the recording process
    - `Arguments`
        - `int index` the index of the device in the `Devices` list
    - `Returns`
        - `void`


- `StartRecording` starts the microphone recording
    - `Arguments`
        - `int frequency=16000` the frequency of the inner `AudioClip`
        - `int sampleLen` the length of a single sample segment that the instance keeps and fires on event
    - `Returns`
        - `void`

- `StopRecording` stops the microphone recording
    - `Returns`
        - `void`


## Contact
[@github](https://www.github.com/adrenak)  
[@www](http://www.vatsalambastha.com)  
[@npm](http://www.npmjs.com/~adrenak)