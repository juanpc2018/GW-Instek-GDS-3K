# GW-Instek-GDS-3K 

GW Instek GDS-3000 series, have 2 groups... </br>
from 150Mhz to 350Mhz with 5GSa/s and 500MHz with 4GSa/s, </br>
the 500MHz has a different HW, different Firmware. </br>

this is only for 150MHz to 350MHz range, 2 or 4 channels, Non-A models "The Original". </br>
GDS-3152 </br>
GDS-3154 </br>
GDS-3252 </br>
GDS-3254 </br>
GDS-3352 </br>
GDS-3354 </br>
A-models are New version, Unkown. </br>

Problem: </br>
SVGA db15 output is 800x600 BUT... Non-Standard 59fps, </br>
500MHz models have same screen, maybe same problem, Unknown. </br>

59fps makes VGA output 100% incompatible with most VGA to HDMI converters, </br>
requires a DSP Scaler, most monitors with VGA input have enough DSP to adapt, </br>
but cheap converters Do Not. </br>
some give Green Screen, others give an image outside screen. </br>
most monitors VGA input is Not isolated, Monitor switching noise affects measurements. </br>
Plastic Monitors are Not Grounded. </br>

tested many cheap & hi quality converters without Scaler, None worked. </br>

Works: </br>
Kramer VP-728 FW 1.29 </br>

Should work: </br>
Kramer VP-729 "Ethernet"</br>
Kramer Newer 4K models: [VP-732](https://www1.kramerav.com/us/Product/VP-732), [VP-778](https://www1.kramerav.com/us/product/vp-778)</br>
Kramer Newer 2K models: [VP-771](https://www1.kramerav.com/us/Product/VP-771), [VP-770](https://www1.kramerav.com/us/Product/VP-770)</br>

Maybe work: "Untested" </br>
Kramer older models: VP-718 719 720 724 xl </br>
AudioAuthority [1366](https://www.cs1.net/products/audio_authority/1366.htm) "VGA to VGA", [1385](https://www.cs1.net/products/audio_authority/1385.htm) "VGA to HDMI" </br>
Startech [VGA2HDPRO2](https://www.startech.com/en-us/audio-video-products/vga2hdpro2) similar to 1385.</br>
Micomsoft XPC-4 </br>
maybe others... </br>

Do Not Work: </br>
Kramer VP-22 "Analog H-V Adjustment, RGBHV to Component BNC" </br>
Audio Authority [9A60](https://www.cs1.net/products/audio_authority/9A60A.htm) "Analog VGA 5-wire RGBHV to Component 3-RCA" similar to Kramer VP-22. </br>

VGA to Component Video do Not accept 800x600 "Standard VGA Signal", </br>
PCIe video card with VGA or [DVI-A](https://en.wikipedia.org/wiki/Digital_Visual_Interface#Connector) output, </br>
driver needs to be forced/tweaked to output compatible NTSC / PAL signals </br>
for "Viewing PC on a TV" </br>
Game Emulators to TVs/Recorders with YPbPr input "Retro Gaming" </br> 

The Good, the Bad & the Ugly: </br>
Kramer VP-728 does Not have enough DSP to do Digital PIP </br>
VGA + HDMI sadly. </br>
Only Universal-Inputs+VGA *see manual. </br>
HDMI Embedded Audio does Not work at 1920x1080 nor 1920x1200 with MacMini 2014. </br>
manual say: does Not work with RGB 1920x1080 but works with 1080p or Native </br>
None Worked probably because Linux was forced at 96Khz, VP-728 is 48Khz. </br>
$ cat /etc/pulse/daemon.conf </br>
default-sample-rate = 96000 </br>
alternate-sample-rate = 96000 </br>

Advantage:  </br>
VP-728 has Detail Enhancement and Chroma Enhancer </br>
both settings at Low, increase quality of HDMI 1080p signals drastically on Smart TVs. </br>
Looking YouTube Videos feels like watching [444](https://www.displayninja.com/chroma-subsampling/) instead of [420](https://en.wikipedia.org/wiki/Chroma_subsampling#Sampling_systems_and_ratios) </br>
Opera Browser has a Lucid Mode 4 similar to Detail Enhacement Low, but needs too much CPU. </br>
DSP is much more efficient. </br>
NTSC looks Ok on a Cellphone, but in large screen 55" FullHD, Enhancements are a must. </br>
also has Luma Enhancement for YUV signals, does Nothing to RGB signal. </br>

has multiple inputs, works as a Small Switcher. </br>
good for PC Monitors that only have 1x HDMI input, No VGA input. </br>
but... </br>
Max Resolution 1920x1200x60 </br>
some features do Not work at High Resolution *Read Manual. </br>

Acceptable: </br>
has a small 1U 12v fan, tolerable, Not as loud / noisy as others. </br>
fanless modification with bigger heatsinks would be nice. </br>
or a bigger 140mm fan on the Top, but No longer 1U. </br> 

Latency:  </br>
Near 0, DSP usually has 4-samples of audio latency,  </br>
when TV is set to Game-Mode and VP-728 to: </br>
Fast Switching, Frame Lock Off.  </br>
Frame Lock On takes more time to Sync the Out clock to the Input clock.  </br>
