# Firmware

Firmware needs to do the following :
 
It needs to deal with devices disappearing and appearing anytime 
 
during runtime
It needs to be prepared to boot any operating systems that are 
 
written for the PC
It needs to wake up if an external stimulus occurs
 
It needs to adjust its backlight, clocks, and speed based on 
 
the temperature, the power source, and the status of the user 
(inactive or active)





However, embedded systems and IoT devices have some unique firmware 
requirements from PC BIOS:
• 
Timeliness in responding to external stimuli (real-time behavior).
The examples are industrial precision machines. These machines 
cannot tolerate any deviation from their specified error margins 
during operation.
• 
Determinism during execution
. The examples are missiles and 
rockets. You probably don’t want to see these things taking 
different software paths every time they fly out of their launch 
pad; who knows what will happen if they act differently every time 
they execute their software after launch? Results might be deadly 
if the software is nondeterministic.

 
• 
Predictability of the outcome
. The examples are industrial 
machines and manufacturing robots. They need to deliver the 
same result repeatedly without deviating from its programmed 
behavior; otherwise, the produced items may not be usable.
• 
Closed system with fixed function
. The examples are the set-top 
box and GPS. The software running inside these things are doing 
one function (or a few functions) very well without errors.
• 
Closed system with limited expansion
. The examples are the Mars 
Rover and home appliances. Once these things are delivered 
(departed Earth or sent home), the software inside should not 
need to deal with components coming and going in the systems, 
because a closed system can safely assume no expansion after 
certain points.
• 
Fast boot time
. The examples are rearview cameras of cars, mobile 
phones, and home appliances. These things need to boot fast 
for either safety reasons or for a better user experience. It was 
very annoying when some early Blu-ray DVD players took a long 
time to be ready to play DVDs, because no consumer electronic 
devices should take more than a few seconds to be ready (at least 
this is not what consumers are used to).
• 
Small footprint
. The examples are wearable devices, sensors, 
and software that needs to be certified. Big software frequently 
needs bigger storage devices, and they tend to be error-prone and 
difficult to certify.
• 
Security and reliability
. The examples are point-of-sale (POS) 
terminals and in-vehicle-infotainment systems (IVI). In IVI, you 
probably don’t want a software crash in the DVD player of the 
system to bring down the GPS, radio, and phone connection, 
and you do not want your credit card information stolen during 
checkout at a store; isolation of mission-critical and nonessential 
elements are, therefore, very important for some applications.
• 
Fixed boot target
. The examples are Chromebook and IVI. 
These devices only have one boot target in mind (ChromeOS or 
embedded Linux); therefore, the firmware does not need to worry 
about having a general-purpose boot loader interface ready to 
boot any OS. A direct-boot interface can not only save code space, 
but also boots faster because shortcuts can be taken.
