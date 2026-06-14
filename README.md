<h1>MacroNova</h1>

<p>So, I decided to build a 4x4 macro pad for Hack Club Macondo, and MacroNova is basically my take on a clean, fully programmable desktop controller. The whole goal here is to cram 16 mechanical switches, an OLED screen, and a bunch of custom shortcuts into a compact, handwired build that makes workflow a lot faster.</p>

<h2>How It Works</h2>
<p>Instead of doing a lazy wiring job and wasting 16 separate GPIO pins on the microcontroller, I am wiring the switches into a <strong>4x4 matrix</strong>. This drops the required pins down to just 8. To make sure the board doesn't register fake keypresses when I smash multiple buttons at once, I am adding a 1N4148 diode to every single switch to block ghosting entirely.</p>

<p>The brain of the project is an <strong>ESP32-S3 DevKit</strong>. Connected to that is an SSD1306 OLED display running over I2C, which will give me live visual feedback on whatever layer or profile is currently active. For the software side, I am flashing CircuitPython and using the KMK firmware framework because it makes updating macros and remapping keys on the fly incredibly easy.</p>

<h2>Current Status</h2>
<p>Right now, I am using this repository to map out the schematics, finalize the pinouts, and put together the official bill of materials so the Macondo reviewers can check it out for funding. Once the parts land, the building and soldering logs go right here.</p>
