<h3>Important points</h3>
<div>
<ul>
  <li>Place Capacitor's as close as possible to the IC that they'll be connecting to for best performance</li>
  <li>Line-up components to ease tracing</li>
</ul>
  <p align="left"><img length="210" width="566" alt="image" src="https://github.com/user-attachments/assets/a074131c-0d25-4b7b-b17f-d6022adef01c"/></p>
</br>
<ul>
  <li>Make sure to route the USB D+ and D- lines first. most important traces. to upload the code. route these traces as a <a href="https://resources.altium.com/p/what-are-differential-pairs-and-differential-signals"><mark>differential pair</a></mark></li>
  <li>trace the USB D+ and D- lines close as possible and the same length. (<a href="https://www.youtube.com/watch?v=ySuUZEjARPY">Video explaining USB protocol</a>)</li>
  <li>Avoid routing any analog signals too close</li>
  <li>Use vias to connect top layer to bottom layer. keep this to a minimum. make use of the top layer.</li>
  <li>For handling ALL ground connections, just break a trace slightly away from the pad and connect a via to the end</li>
  <li>Fill the PCB with a gound plane (Copper zone). All the ground vias will be connected.</li>
  <li><a href="https://www.youtube.com/watch?v=OwbWVQkONH4&t=1s">How to connect multiple circuit boards using mouse-bite on KiCad?</a></li>
  <li>Place extra ground vias all around for adequate thermal relief</li>
  <li>Check for clearance, hole sizes, thermal</li>
  <li>Most clearance can be ignored since it might be between holes and pads on pre-built footprints. Adjust the once that was placed by us.</li>
  <li><a href="https://www.pcbway.com/QuickOrderOnline.aspx">Check for drilling hole sizes recommended, etc.</a></li>
  <li>For any “track has unconnected end" errors, you should just click on them and delete them manually</li>
  <p align="left"><img alt="image" src="https://github.com/user-attachments/assets/409de555-b8d6-4077-82c6-538628409169"/></p>
  </br>
  <li> For any thermal errors, they can be easily fixed by adding some extra traces going out.</li>
  <p align="left"><img alt="image" src="https://github.com/user-attachments/assets/9dc0ff76-90f9-47bc-8add-2a71a8a2816e"/></p>
</ul>
 </div> 

