<h1>MacroNova</h1>
<p>So, I decided to build a 4x4 macro pad for Hack Club Macondo, and MacroNova is 
basically my take on a clean, fully programmable desktop controller. The whole goal 
here is to cram 16 mechanical switches, an OLED screen, and a bunch of custom 
shortcuts into a compact, handwired build that makes workflow a lot faster.</p>

<h2>How It Works</h2>
<p>Instead of doing a lazy wiring job and wasting 16 separate GPIO pins on the 
microcontroller, I am wiring the switches into a <strong>4x4 matrix</strong>. This 
drops the required pins down to just 8. To make sure the board doesn't register fake 
keypresses when I smash multiple buttons at once, I am adding a 1N4148 diode to every 
single switch to block ghosting entirely.</p>

<p>The brain of the project is an <strong>ESP32-C3-DevKitM-1</strong>. Connected to 
that is an ER-OLEDM0.91 display running over I2C, which will give me live visual 
feedback on whatever layer or profile is currently active. Two 4.7kΩ pull-up resistors 
sit on the SCL and SDA lines to keep I2C communication stable and reliable. For the 
software side, I am flashing CircuitPython and using the KMK firmware framework because 
it makes updating macros and remapping keys on the fly incredibly easy.</p>

<h2>Current Status</h2>
<p>Schematic is fully complete. The 4x4 key matrix, diode placement, OLED wiring, I2C 
pull-up resistors, and all ESP32-C3 pinouts are finalized and verified. The bill of 
materials is ready for Macondo reviewers. Waiting on funding approval — once parts 
arrive, build and soldering logs go right here.</p>
<img src="images/Screenshot 2026-06-16 221625.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 221618.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 221613.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-15 184501.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-15 184453.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 221656.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223902.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223910.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223915.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223924.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223928.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 223944.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 224001.png" alt="Schematic" width="700">
<img src="images/Screenshot 2026-06-16 224004.png" alt="Schematic" width="700">
