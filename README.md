# Useful 3D printer commands

## PID Calibration

- Export Current Settings
  - Run `M503` and record the current value for backup.  
    Example output:  
    `M301 P18.93 I0.91 D98.07`

- Start the Autotune process  
    `M303 E0 S230 C5`  

    Example output:  

    ```
    Recv: PID Autotune finished! Put the last Kp, Ki and Kd constants from below into Configuration.h
    Recv: #define DEFAULT_Kp 12.90
    Recv: #define DEFAULT_Ki 0.55
    Recv: #define DEFAULT_Kd 75.57
    ```

- Take PID out and enter into system  
    `M301 P12.90 I0.55 D75.57`

    Example output:

    ```
    M301 P12.90 I0.55 D75.57
    ```

- Save the new values  
    `M500`

    Example output:  

    ```
    Send: M500
    Recv: ok
    ```
