# zdkaudio.h

```c
/* Initialization */
HRESULT WINAPI ZDKAudio_Initialize();
HRESULT WINAPI ZDKAudio_Shutdown();

/* Control Voices */
HRESULT WINAPI ZDKAudio_CreateVoice(const WAVEFORMATEX *format, DWORD formatSize, HVOICE *handle);
HRESULT WINAPI ZDKAudio_DestroyVoice(HVOICE handle);

/* Playback Control */
HRESULT WINAPI ZDKAudio_GetPan(HVOICE handle, float *pan);
HRESULT WINAPI ZDKAudio_GetPitch(HVOICE handle, float *pitch);
HRESULT WINAPI ZDKAudio_GetVoiceState(HVOICE handle, ZDK_VOICE_STATE *state);
HRESULT WINAPI ZDKAudio_GetVolume(HVOICE handle, float *volume);
HRESULT WINAPI ZDKAudio_Pause(HVOICE handle);
HRESULT WINAPI ZDKAudio_Play(HVOICE handle);
HRESULT WINAPI ZDKAudio_SetMasterVolume(float volume);
HRESULT WINAPI ZDKAudio_SetPan(HVOICE handle, float pan);
HRESULT WINAPI ZDKAudio_SetPitch(HVOICE handle, float pitch);
HRESULT WINAPI ZDKAudio_SetVolume(HVOICE handle, float volume);
HRESULT WINAPI ZDKAudio_Stop(HVOICE handle, BOOL immediate);

/* Send Audio Data*/
HRESULT WINAPI ZDKAudio_SubmitPacket(HVOICE handle, const BYTE *data, DWORD dataSize, int loopStart, int loopLength, int loopCount);

/* Types */
typedef enum {
	VOICE_STATE_PLAYING = 0x1,
	VOICE_STATE_STOPPING = 0x2,
	VOICE_STATE_STOPPED = 0x4,
	VOICE_STATE_PAUSED = 0x8
} ZDK_VOICE_STATE;
```


---
[[OpenZDK Reference]]