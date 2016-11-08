#Introduction to Physical Computing with Arduino

developed for:

##[Introduction to Physical Computing with Arduino Workshop](https://gcdi.commons.gc.cuny.edu/workshops/)

November 9th, 6:30-8:30pm

Instructors: Mary Catherine Kinniburgh + Jojo Karlin!

*Adapted from [A Super-Speedy Intro to Maker Basics with Arduino](https://github.com/mckinniburgh/QuickStartPhysComp), a tutorial designed for #dhpraxis2016.

*Thanks to Tiffany Chan for her inspiring and helpful [Arduino Tutorial](https://github.com/uvicmakerlab/dhsi2016/blob/master/ArduinoNotes.md) for [Digital Humanities Summer Institute 2016](http://www.dhsi.org/index.php), in Jentery Sayers' Physical Computing and Desktop Fabrication Class. 

##GC Resources at a glance:

####[Monday Maker Hours](https://gcdi.commons.gc.cuny.edu/monday-maker-hours/)

Alternating Mondays, 2:00-4:00pm in Room 7414. Open lab time for experimenting, projects, prototyping, saying hello!

####[GC Maker Space](https://gcdi.commons.gc.cuny.edu/gc-maker-space/)

Located in the GC Digital Scholarship Lab, Room 7414. Monday Maker Hours, workshops, and consults for all levels and disciplines.

#Overview

##Workshop Goals:

**In this workshop, we will:**

* Learn about maker spaces, critical making, and physical computing practices in higher education and beyond

* Become familiar with Arduino's vocabulary and basic setup

* Build a basic circuit and run a basic program on the Arduino

* Add complexity to our circuits to begin using more types of sensors and actuators

* ...and conceive of further possibilities for physical computing-style projects. 


1. [Why Make?](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#why-make)

   +[Key Term: Maker Space](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#key-term-maker-space)
   
   +[Key Term: Critical Making](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#key-term-critical-making)
   
   +[Key Term: Physical Computing](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#key-term-physical-computing)
   
   
2. [Basic Vocabulary](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#basic-vocabulary)

3. [Setting up Arduino](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#setting-up-arduino)

4. [Activity: Arduino LED](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#activity-arduino-led)

5. [LED Bonus Round: Using Resistors](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#led-bonus-round-using-resistors)

6. [Activity: Arduino toneMelody](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#activity-arduino-tonemelody)

7. [Activity: Add a Button!](https://github.com/mckinniburgh/gc-phys-comp/blob/master/IntroPhysCompArduino.md#activity-add-a-button)

##Why Make?

###Key term: **Maker Space**

Definition: 

any physical space that offers access to hands-on equipment to produce prototypes of physical objects.

_What separates a maker space from a production line (although some large-scale maker spaces have this capacity) is that maker spaces are where you go to *experiment, prototype, and think* with materials_ 

+[NYDesigns](http://nydesigns.org/) is modeled on a business incubator/start-up model for industry research. 

+[Maker Lab in the Humanities, University of Victoria](http://maker.uvic.ca/twoyears/) is a research-focused lab that “prototypes the past” in order to historicize technologies and their developmental arcs. 

+[Critical Making Lab, University of Toronto](http://criticalmaking.com/about/), argue for “critical making” as a way to reflect critically on questions of technology, society, and culture in the process of making.

+[Makerspace at U.Va](http://scholarslab.org/makerspace/) acts as an educational outreach environment that offers workshops, drop-in hours, and consultations designed to connect students with resources. 

Antecedents to the university makerspace:

[hackerspace](http://hackerspaces.org/): the maker space’s more programming-focused counterpart (or predecessor, depending on how you view it)

[“hacking”](https://en.wikipedia.org/wiki/Hacker_culture): in a positive sense, alters technologies for creative uses and greater accessibility. This led to early hackerspaces incorporating circuitry, microcomputing platforms, and other hardware.

####The process, rather than the product, defines the space.

###Key term: **Critical Making**

Research that uses the act of 'making' (as in maker spaces) to critically reflect on the materials, social implications, and cultural factors implicit in the process of building digital projects.

[Examples of critical making projects from University of California Berkeley](http://make.berkeley.edu/spring-2016/)
	-largely theoretical; ways to think about technology

###Key term: **Physical Computing**

Definition:

Physical computing takes “the human body and its capabilities as the starting point, and attempt[s] to design interfaces, both software and hardware, that can sense and respond to what humans can physically do” (Tom Igoe, “What is Physical Computing”).

+ A popular point of inquiry for critical making and process-oriented prototyping

![Physical computing feedback loop](https://github.com/mckinniburgh/QuickStartPhysComp/blob/master/images/Physical_computing.svg.png)

*image made by Nevit Dilmen for the physical computing [Wikipedia](https://en.wikipedia.org/wiki/File:Physical_computing.svg) page*

Examples:

-[GPS Jacket](https://learn.adafruit.com/flora-gps-jacket/overview)

-[Beet Box](https://vimeo.com/55658574)

-[Electromagnetic Field Sampler](http://makezine.com/projects/weekend-project-sample-weird-sounds-electromagnetic-fields/)

-[More Examples from Tom Igoe's "Physical Computing's Greatest Hits (and misses)"](http://www.tigoe.net/blog/category/physicalcomputing/176/)

##Basic Vocabulary

+ *Arduino:* consists of a microcontroller (or programmable circuit board) that comes with software (an IDE) that allows you to write code and upload it to the board. Arduino is an [open source project.](https://www.arduino.cc/en/Guide/Introduction)

+ *IDE:* Integrated Development Environment, or software application with a source code editor, debugging, and other tools. The Arduino IDE is the software that holds your code, as opposed to the Arduino Board, which contains your circuits.

+ *Sketch:* this is Arduino's term for a program--a piece of code that is fed to the Arduino board through USB.

+ *LED:* light-emitting diode. In circuits, diodes make electricity flow in one direction only. This accounts for the importance of *cathode* and *anode* parts of your LED bulb--more on that later!

+ *Resistor:* a device used in circuits that "resists" electricity flow. The [stripes on the resistor](https://learn.adafruit.com/adafruit-arduino-lesson-2-leds/resistors) determine its unit of resistance, measured in ohms. 

+ *Ground:* the reference point from which voltage is measured. 

+ *Breadboard:* a tool for solderless prototyping that makes rewiring simple. 

+ *Sensor*:

+ *Actuator*:

	For a more thorough introduction to breadboards, see: [https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard)
	
##Setting up Arduino

1. Take your Arduino and plug in the USB cable to both the Arduino and your computer.

2. Open up Arduino IDE on your computer. Look for this logo:

![logo](https://github.com/mckinniburgh/QuickStartPhysComp/blob/master/images/Arduino.png "Arduino Logo")

3. Set up board

Go to `Tools`

Select `Board: Arduino/Genuino Uno.`

This is the type of Arduino we're using today

4. Set up port

Go to `Tools`

Select `Port`

Choose `/dev/cu.usbmodem1411 (Arduino/Genuino Uno)`
	

Now you're ready to make circuits! 

#Activity: Arduino LED

**Supplies**

+ Arduino
+ 2 wires
+ 1 LED bulb
+ Breadboard
+ Resistor

##**The Circuit**

Don't forget to unplug your Arduino as you wire your circuit! This keeps your computer safe. 

![Circuit Diagram](https://github.com/mckinniburgh/gc-phys-comp/blob/master/Images/BasicLED_bb.png)

*This circuit was made from [Fritzing](http://fritzing.org/home/)*

You'll take a wire from your *ground*, or the 5V slot on the Arduino board, to the (-) power rail of the breadboard. 

Then, place a resistor with one "leg" in the (-) power rail of the breadboard, and the other horizontally in line with the *anode* (long side) of the LED. Make sure the LED has its anode and cathode in different terminal strips (vertically aligned on breadboard)!

![Anatomy of an LED](https://github.com/mckinniburgh/QuickStartPhysComp/blob/master/images/LED-image.jpg "http://sciencewithkids.com/science-facts/facts-about-LEDs.html")

Next, connect another wire to the *cathode* (short side) of the LED, and place this in pin 8 on the Arduino board.

##**The Code**

Arduino has ready-to-go code, which we'll use to get started today. You can open their examples and then edit the code as you like. 

1. Go to `File --> Examples --> 01.Basics --> Blink`

2. Open the `Blink Sketch` and check out the code. 

3. In `void setup( )` we're going to initialize `pin 8` as our output. Change `LED_BUILTIN" or 13,` depending on your version of Arduino's IDE, to `8`.

4. In `void loop( )` change `LED_BUILTIN` to `8` as well. 

5. **Verify** your sketch with the check-mark in the upper-left hand corner of the window
    Troubleshoot: have you selected your proper board and port? Is the Arduino plugged in? Have you double-checked your circuits?
    
6. **Upload** your sketch and watch the LED blink!

####Bonus points: change the speed of the LED blinking by adjusting the delay value.     

#LED Bonus Round: Using Resistors

Resistors 
Experiment with rewiring the circuit *without* the resistor and notice what happens. 

You have another type of resistor in your supply bag--give this one a shot and see how it affects your circuit. 

#Activity: Arduino toneMelody

1. Go to `File --> Examples --> 02.Digital --> toneMelody`

2. Open the `toneMelody` sketch and check out the code. 
 
3. In your supply kit, you'll find a small piezo buzzer. Wire the circuit using the piezo instead of the LED, using the same diagram above. 

#Activity: Add a Button!

Now that we're more familiar with basic wiring, we'll add a button to our circuit so we can turn an LED or piezo on and off. 

#Quick recap:

##Revisiting Workshop Goals:

**In this workshop, we:**

* Learned about maker spaces, critical making, and physical computing practices in higher education and beyond

* Became familiar with Arduino's vocabulary and basic setup

* Built a basic circuit and ran a basic program on the Arduino

* Added complexity to our circuits to prepare for accommodating more types of sensors and actuators

* ...and considered further possibilities for physical computing-style projects. 

#To keep on learning...

Join us at [Monday Maker Hours](https://gcdi.commons.gc.cuny.edu/monday-maker-hours/) at the [GC Maker Space](https://gcdi.commons.gc.cuny.edu/gc-maker-space/), located in the [GC Digital Scholarship Lab](https://gcdsl.commons.gc.cuny.edu/), Room 7414 at The Graduate Center, CUNY. We have Arduinos, a variety of sensors, LEDs, piezos, and other physical computing equipment for experimenting and project prototyping. All levels and perspectives welcome! [Contact us](https://docs.google.com/forms/d/e/1FAIpQLSeLwRoCkz5NPPLh0vYMOQPqyA5H3fbWn5ga2-F8M-pQvrg5IA/viewform?c=0&w=1) for more information. 

#One more thing: we want your feedback!

##Please fill out our feedback form [here](https://docs.google.com/forms/d/e/1FAIpQLSfNW2FJXd236V3zCtJXHLiJrKETEXqVms-qTxHaYN_h8GCA_A/viewform). Thank you for coming to our workshop!