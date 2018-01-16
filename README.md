# spectre_meltdown

Processor vulnerability proof of concepts. I did not create these PoCs but have modified one slightly and have used them to perform some basic research relating to Microsoft's mitigations for Windows and provided some example screenshots below.

- Spectre bounds check bypass and branch target injection vulnerability (CVE-2017-5715, CVE-2017-5753) requires a firmware (microcode) update.
- Meltdown rogue data cache load vulnerability (CVE-2017-5754).

SANS Link. https://isc.sans.edu/forums/diary/Meltdown+and+Spectre+clearing+up+the+confusion/23197/

## Usage for ca.exe
- `ca.exe <offset integer>`

e.g. 
- `ca.exe 1000`

## Usage for spectre.exe
- `spectre.exe`

## Before patching ca.exe screenshot

![ca.exe screenshot](https://github.com/bao7uo/spectre_meltdown/raw/master/images/ca_screenshot.png)

## Before patching spectre.exe screenshot

![spectre.exe screenshot](https://github.com/bao7uo/spectre_meltdown/raw/master/images/spectre_screenshot.png)

## After patching ca.exe

PoC still works.

## After patching spectre.exe screenshot

No microcode update, so it seems like Microsoft have implemented some kind of AV mitigation. The successful execution is from an AV excluded folder.

![spectre.exe screenshot](https://github.com/bao7uo/spectre_meltdown/raw/master/images/spectre_after_screenshot.png)
![spectre.exe screenshot](https://github.com/bao7uo/spectre_meltdown/raw/master/images/spectre_av_screenshot.png)
