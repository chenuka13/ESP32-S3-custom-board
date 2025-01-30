<p>Obtain the schematics for the microcontroller from the datasheets</p> 
<p>Searching for datasheets that allign with the WROOM/modulw with other componenets, which is the <a href="https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32s3/esp32-s3-devkitc-1/index.html">DevKit datasheet</a></p>
<p>Obtain the ESP32-S3 <a href="https://dl.espressif.com/dl/schematics/SCH_ESP32-S3-DevKitC-1_V1.1_20221130.pdf">DevKit schematic</a></p>
<div>
  <img alt="image" src="https://github.com/user-attachments/assets/3d95ecce-4ae9-4c4f-a01b-066144e4095d"/>
</div>
<div>
<p>Checkout the <a href="https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf">general ESP32-S3 datasheet.</a> There you will find that the chip supports USB communication and provides us with the necessary pin lines.</p>
  <img alt="image" src="https://github.com/user-attachments/assets/ffcea0f6-4e20-4608-823b-fb184cc38657"/>
  <img alt="image" src="https://github.com/user-attachments/assets/82d1c108-edc5-4d6b-8972-8dd7ac7a3f35"/>
</div>
</br>
<p><b><i><mark>This indicates that we can completely bypass the USB-to-UART IC in the schematic</mark></i></b></p>
<div>
  <img alt="image" src="https://github.com/user-attachments/assets/de38966d-4197-431d-9bf0-6cae51b31455"/>
</div>
</br>
<p>include details on how we can remove the zener diodes on the USB-C line and why its better to have it</p>
<p><i>Resources for downloading free IC footprints and schematic symbols can be found at <a href="https://www.snapeda.com/">SnapEDA.</a></i></p>
<div>
  <p>How to connect a USB-C port instaed of the original USB in the schematic</p>
  <img alt="image" src="https://github.com/user-attachments/assets/a15596c2-2957-4f7e-b852-ce9844cffdee"/>
</div>

<div>
  <p>Adapting to a AMS1117 voltage regulator instaed of the SGM2212 IC used in the original schematic</p>
  <img alt="image" src="https://github.com/user-attachments/assets/ecdd73af-a53e-4e31-8d68-3ef3fd1ac2e7"/>
  <p>Always refer to the datasheet in case any additional components have to be added for functions. Refer to the 'Typical application circuit' in the specific datasheet</p>
</div>
</br>
</br>
<p>If you’re ever in doubt about how you should decouple a power line, it’s (generally) a good rule of thumb to use a <mark>10uF and 0.1uF/100nF capacitor in parallel</mark> since they will cover a large range of frequencies. This is good for smoothening out the voltages of any unwanted noise/spikes.</p>

<h3>Resulting customized schematic design</h3>
<p align="center"><img alt="image" src="https://github.com/user-attachments/assets/105564e9-d1e7-401c-9c77-a4c39a521d11"/></p>
</br>
<p> Most of the time you need to press the reset (RST) button in order to get the board going. This can be super inconvenient in situations when you may not have easy access to the button such as when it’s in a 3D-printed enclosure.This was resolved by adding 10K pull-ups to the BOOT/RST lines. This bug is also in a lot of commercial DevKits.</p>
<p align="center"><img alt="image" src="https://github.com/user-attachments/assets/f6ade273-f403-49f0-ab69-e65bcf5ba5e8"/></p>







