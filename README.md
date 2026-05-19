# RTCC_18FxxJ50 library

Library for accessing the PIC18FxxJ50 internal RTCC. The library should be compatible with other PICs with same RTCC.

## Features:
- Get/Set RTCC/Alarm
- Get RTCC/Alarm/ElapsedTimeToAlarm as string
- BCD and Dec versions of Get / Set routines for RTCC/Alarm/ElapsedTimeToAlarm
- Alarms can be masked to trigger at different intervals
- Designed for use with DeepSleep
- Backup library configuration state to DeepSleep persistent registers
- Compiler directive for synchronizing RTCC/Alarm register reads with RTCSYNC bit
- Compiler directive for synchronizing RTCC/Alarm register writes with RTCSYNC bit
- Compiler directive for updating RTCC DateTime registers in Read‐Modify‐Write fashion
- Compiler directive for double sampling RTCC DateTime registers on reading
- Compiler directive for saving library configuration state to DeepSleep persistent registers

## Requirements / Recommendations:
- If using DeepSleep, RTCCConfiguredAfterPowerUp variable must be reset to 0 on PIC init.
- If using DeepSleep, RTCCConfiguredAfterPowerUp variable may be saved to DeepSleep persistent registers, to preserve the information about RTCC "configured state", to avoid reconfiguring after wake‐up.

## Limitations:
- GetRTCCElapsedToNextAlarm BCD/Dec routines do not take into account the alarm mask

## Other:
Initially uploaded to LibStock: https://libstock.mikroe.com/projects/view/16/rtcc-18fxxj50-library


---


#RTCCP24EP library

Library for accessing the PIC24EP internal RTCC. The library should be compatible with other PIC24EPs with same RTCC.
## Status:
in work