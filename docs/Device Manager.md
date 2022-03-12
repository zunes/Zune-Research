# Device Manger
The device manager loads device drivers and manages their resources.

## Security
**Taken from** [Microsoft - Device Manager Security](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee484890(v=winembedded.60)):
In Windows Embedded CE 6.0, the kernel performs a full access check on first level buffer pointer parameters. This access check eliminates the need for validation to be performed by the device driver. However, a driver must still verify that the caller has access to memory addressed by embedded pointers using [CeOpenCallerBuffer](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee488382(v=winembedded.60)) and [CeCloseCallerBuffer](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee488934(v=winembedded.60)). For additional information, see the [Migrating a Windows Embedded CE Driver to Windows Embedded CE 6.0](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee485224(v=winembedded.60)).


## References
- [Microsoft - Device Manager Architecture](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee484004(v=winembedded.60))
- [Microsoft - Device Manager Security](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/ee484890(v=winembedded.60))

---
[[Windows CE 6.0]]