# RT880-FlasherX

A (hopefully) cross platform .bin firmware flasher for the Radtel RT-880 and iRadio UV-98.

There's a whole bunch of platforms in [releases](https://github.com/nicsure/RT880-FlasherX/releases).

Download the one for your system and run the "RT880-FlasherX" executable inside.

## Running the Application

### Windows Users

Run the appropriate `.exe` file and click 'Run anyway' at the security prompt.

### Mac Users

Run this command from a terminal inside the root folder:

```bash
chmod +x RT880-FlasherX && xattr -cr . && for f in *.dylib RT880-FlasherX; do codesign -f -s - "$f" 2>/dev/null; done && ./RT880-FlasherX
```

This grants the file execute permissions, signs the binaries and UI files and runs the program. All of these steps are needed to run on modern MacOS.

### Linux Users

Give the file execute permissions and give yourself access to serial ports, on Linux this is by adding yourself to the 'dialout' group  

```bash
sudo chmod +x RT880-FlasherX && sudo usermod -a -G dialout <your_username>
```
