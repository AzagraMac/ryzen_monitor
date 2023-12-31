# ryzen_monitor
Monitor power information of Ryzen processors via the PM table of the SMU.

This tool is based on the [ryzen_smu](https://github.com/AzagraMac/ryzen_smu) kernel module for reading the PM Table from the SMU. It is a continuation of the demo-tool provided with that project.

**ryzen_monitor** features support for multiple PM table versions (i.e. multiple bios versions), adds support for Ryzen 5000, and presents more fields to user. It is especially focused around providing a more realistic image of the actual power draw and hence true thermal output of the CPU package.

## Supported CPUs
* Ryzen 5000 series
  * Ryzen 9 5950X
  * Ryzen 9 5900X
  * Ryzen 7 5800X
  * Ryzen 5 5600X 
  * Ryzen 7 5700G
  * Ryzen 5 5600G
* Ryzen 3000 series
  * Ryzen 7 3700X
  * Ryzen 9 3900X
  * Ryzen 9 3950X
  * Other non-Threadripper models will probably work, but are untested

Note: Support also depends on the PM table version that ships with your BIOS and whether ryzen_monitor already knows how to read it.

## Screenshot
![Captura desde 2023-06-10 17-51-26](https://github.com/AzagraMac/ryzen_monitor/assets/571796/3d8fa524-d09e-4325-930b-7e1526997d4f)


## Building
First install the kernel module from [ryzen_smu](https://github.com/AzagraMac/ryzen_smu).

Then pull and make **ryzen_monitor**:
```bash
git clone https://github.com/AzagraMac/ryzen_monitor.git
cd ryzen_monitor/
make

sudo ./src/ryzen_monitor
```
Enjoy!

## About the quality of the provided information
Don't rely on the information given by this tool.

To my knowledge there is no official documentation on how to do this. Everything was created by starring at numbers, a lot of guesswork and finding fragments somewhere on the web. It is possible that some assignments or calculations are incorrect.

This program is provided as is. If anything, it is a toy for the curious. Nothing more. Use it at your own risk.

Regards to Florian Huehn <hattedsquirrel@gmail.com> 
