# zdkinput.h
```c
/* Initialization */
HRESULT WINAPI ZDKInput_Initialize();
HRESULT WINAPI ZDKInput_Shutdown();

/* State */
HRESULT WINAPI ZDKInput_GetState(ZDK_INPUT_STATE *state);
/* ZDKInput_GetNextInputMessage */
/* ZDKInput_EnableInputMessages */

/* Types */
typedef struct {
	int X;
	int Y;
	int Z;
} ZDK_ACCELEROMETER_STATE;

typedef struct {
	unsigned int Id;
	float X;
	float Y;
	float Pressure;
} ZDK_TOUCH_LOCATION;

typedef struct {
	int Count;
	ZDK_TOUCH_LOCATION Locations[4];
} ZDK_TOUCH_STATE;

typedef struct {
	ZDK_TOUCH_STATE TouchState;
	ZDK_ACCELEROMETER_STATE AccelerometerState;
} ZDK_INPUT_STATE_HD;

/* Zune SD types for dpad have been omitted but can be found in the original header file*/
```

---
[[OpenZDK Reference]]
