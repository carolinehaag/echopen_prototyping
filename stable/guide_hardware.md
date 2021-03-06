# Download repo github : prj\_medtec-kit


A [list of supplies by supplier has been prepared](https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/miscellaneous/general_BOM).

For the BOM, note that the Farnell BOM is only for a laboratory power supply if needed. Moreover, the hackspark BOM is for "basic" fournitures (for soldering), and for sockets (needed for the kit), therefore it is mainly for showing what can be bought in the closest electronic store.

![@todo - AJOUTER UN SCHÉMA D’ATTRIBUTION DES PISTES]()

## **Mother board**

Ref : RS 528-0661 
@todo where does this ref come from?

The original stripboard presents 39 vertical tracks

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_102911.jpg)

We need 19 tracks cut on the track of the middle of the board so that 19 tracks can be preserved, composing the base of the motherboard. One can use a dremel and then smooth the cut. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_103225.jpg)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_103230.jpg)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_103333.jpg)

### *Sockets *

We use 0.1" sockets to connect the daughter boards to the motherboard

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_104039.jpg)

### Preparation

For this, we'll be needing 9 sockets of size 1x19

* first socket on one border (1) for power supply
* second socket on (6)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/1_Mother_board/IMG_20170315_104927.jpg)

## Power supply

See the medkit folder [here](https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/daughter_boards/DB-supply/DB-supply_v1).

### BOM 

[To download the BOM, refer here](https://github.com/echopen/PRJ-medtec_kit/blob/master/electronic/daughter_boards/DB-supply/DB-supply_v1/src/DB-supply_v1.csv).

* PCB : [DB\_Supply\_v1](https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/daughter_boards/DB-supply/DB-supply_v1) (custom echOpen)

@todo: what does it mean?

Locations of each component are indicated on the PCB.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0661.JPG)

#### Capacitors 

They are polarized white side corresponds to lowest potential and must be plugged on white part of the mark on the PCB

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0663.JPG)

#### Integrated circuits 

The dot on the component must be plugged where there is a « line break » (see below for direction)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0665.JPG)

#### Voltage regulator 

They must be plugged according to the mark on the PCB,
i.e. additionnal rectangle corresponds to the part of the voltage
regulator that has sort of a « growth »

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_20170315_113424.jpg)

#### LED

See scheme below to identify the cathode

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/LED.png)

On the PCB, there is an additionnal line where the cathode must be
plugged

#### Transistor 

Match the small strip with the footprint 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_20170315_111947.jpg)

#### Diods

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0661.JPG)

Beware in terms of direction. A line marks the correct side, which is also marked on the PCB footprint. 

@todo: *Resistors : Tableau code couleur ?*

In case of mistake, use the solder wick to remove the solder. Put the wich on the connection, then apply the soldering iron over it. Push a bit on the pins to remove the component maintained in place by remaining solder. 


All components are now in place! 

### Testing the board

The board we've just made is a power-supply board that has several stabilized voltages. It can be tested by powering it properly and checking that output voltages are correct.
So as to power it, one will use a lab power supply, offering a good protection against shorts.
 
![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0669.JPG)

We choose the ideal tension model (C.V) and a 18V tension (which correspond to two 9V batteries that will power the circuit) and the current capped to 800mA.

@question: why two 9V batteries? Why not a 12V or a 5V supply?
 
![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0668.JPG)

This power supply can be plugged to pins 1 and 12 (respectively GND and 18V) 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0670.JPG)

When powering on the supply, the power supply should indicate a current use of 45mA. 

@todo haven't found a picture


![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_0668.JPG)

We then measure tensions between GND (pin 1) and pins 2, 6, 8, 18, 19. To do this, a voltmeter is enough (or an oscilloscope). The respective tensions shoudld be 5V, 12V, -12, -5V and 3.3V.

If one of these tensions is missing, one has to check that all component is rightly positionned and that soldering is well done. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_20170315_111632.jpg)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/2_power_supply/IMG_20170315_111947.jpg)

Once the board validated, one can trim the remaining legs. 

## **High voltage**

### Assembly 

#### BOM 

* [See the BOM](https://github.com/echopen/PRJ-medtec_kit/blob/master/electronic/daughter_boards/DB-high_voltage/DB-high_voltage_v1/src/DB-high_voltage_v1.csv)
* [See full repo reference](https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/daughter_boards/DB-high_voltage)

#### PCB 

See DB-high\_voltage (it's a custom-made, echOpen specific)

#### SMA connector 

The three legs/connectors have to match the three marks on the front side of the PCB, and the two will match the back of it.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/3_High_voltage/IMG_20170315_153217.jpg)

Beware! Check that C14 can stand 100V. 

#### Finished board

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/3_High_voltage/IMG_20170315_160124.jpg)

### *Tests*

Beware! One has to use a 100V-tolerant oscilloscope, or to use a 10x probe.

Ground is up:

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/3_High_voltage/IMG_20170315_161755.jpg)

We should get -90V on the output.

## **Pulser**

### BOM

See [BOM](https://github.com/echopen/PRJ-medtec_kit/blob/master/electronic/daughter_boards/DB-pulser/DB-pulser_v2/src/DB-pulser_v2.csv) or the [full repo for documentation](https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/daughter_boards/DB-pulser)


### Assembly 

This daughter uses an external pulser : the _MAX4940 evaluation kit_, that is connected to the daughter via the P3 connector.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170315_164106.jpg)

@todo Intégrer chéma du MAX4940 :

<https://github.com/echopen/PRJ-medtec_kit/tree/master/electronic/modules/hardware/MDL-pulser/MDL-pulser_v2>

@todo ATTENTION : ERREUR SUR LE SCHÉMA, VEE DOIT ÊTRE RELIÉ AU -12V DE LA DAUGHTER, ET VCC AU +12V A CHANGER SUR LE SCHEMA

Connect the GND to pins 2 and 3 and VPP1 :

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170315_162614.jpg)

Plug components on the pulser daughter board. 

Connect the MAX4940 to the daughter board as shown below :

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170315_162614.jpg) 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170316_120338.jpg) 

The high voltage is connected as follows : blue wire corresponds to the
(+), white corresponds to the ground.

### *Tests*

To test and try the pulser module, connec the output of the board (P6) to the oscilloscope.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170316_114545.jpg)

A 5V logic signal of 140ns has to be injected: to do this, we can connect the motor control unit with the testing code to the motherboard.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/IMG_20170328_183729.jpg)

The output signal of the pulser must have the same duration that the logic input, with an amplitude of -90V. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/4_Pulser/TEK0026.JPG)

## **TGC + T/R switch**

### BOM 

<https://github.com/echopen/PRJ-medtec_kit/blob/master/electronic/daughter_boards/DB-tr_switch_tgc/DB-tr_switch_tgc_v1/src/DB-tr_switch_tgc_v1.csv>

### Assembly 

To solder the SMD components, one can put a small amount of solder 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/IMG_20170316_144737.jpg)

then use a _pince brucelles_ to ensure the component stays in place during soldering. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/IMG_20170316_122800.jpg)

Op-Amp: the mark on left of the figures must match the dot 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/IMG_20170316_144737.jpg)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/IMG_20170316_122624.jpg)

### *Tests T/R switch*

* Connect all daughter boards to the motherboard
* Connect the pulser SMA output to the input SMA of the T/R switch
* Connect track 9 of the motherboard to the oscilloscope input 1
* COnnect test point W1 of the T/R switch to input 2 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/IMG_20170328_184945.jpg)

Here's what you should obtain

 ![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TEK0028.JPG)

* Visualize pulsr command on Channel 1 and the T/R switch W1 point on Channel 2. 

Example of the signal if the T/R switch has burnt: the pulse to the transducer will be -20V instead of -100V

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/TEK0029.JPG)

What you'll see:

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/TEK0029.JPG)

@todo this picture above is not the good one, we don't have it

* Connecte a transducer on the second SMA output of the pulser and put it in an aquarium
* Check the transducer points (P4 or P7 on the pulser) on Channel 1
* Check T/R switch test point W1 on channel 2 

An echo can be seen on both channels:

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/TEK0032.JPG)

### Connecting the TGC

* Solder two wires, one on +5V and the other on GND (for the power supply)
* Solder the two header pins on GAIN and GND so that wires can be connected - or, if you need, to solder the wires directly. They will be connected staight on the red pitaya for gain control. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/IMG_20170328_191304.jpg)

* Connect the TGC IN of the T/R switch on TGC INH 
* Connect the TGC OUT of the T/R switch on TGC VOUT
* Connect 5V and GND of the TGC on the tracks 2 and 1 of the motherboard

### Connections

Note, switchs position of the TGC:

* switch LNA EN on EN
* switch VGA EN on EN
* switch GN SLOPE on UP
* switch GN HI LO on LO


### Tests

* Examine T/R switch test point W1 on channel 1
* Examine TGC out from motherboard (track #3) on channel 2. An amplified echo (around 2V) should be visible. 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/TEK0033.JPG)

## **RedPitaya**

### Connectiques (to do three times)

* Cut a male-male SMA cable in half
* Remove the end of the cable 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/IMG_20170328_192324.jpg)

* With a flat screwdriver, dissamble the metal protection
* Roll them together 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/IMG_20170328_192401.jpg)

* Remove the protection from the center cable

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/IMG_20170328_192452.jpg)

* Connect the cables to a wire (that'll be the ground)
* Connect the center to another (that'll be the signal) 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/5_TR_switch/TGC/IMG_20170328_192539.jpg)

* Connect RedPitaya In1 to the tracks 3 and GND of the motherboard 
* Connect RedPitaya In2 to the tracks 4 and GND of the motherboard 
* Connect RedPitaya OUT1 to the TGC IN and GND 

## Overall configuration including all modules 

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/configuration/IMG_20170331_174120.jpg)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/configuration/IMG_20170331_174204.jpg)

## RedPitaya and Arduino codes installation

### Assembly

* Format the RedPitaya SD card in FAT-32
* Refer to the instructions available on our GitHub repo to install

### Resources

* [Documentation is on the __PRJ-medtec_kit__ repo](https://github.com/echopen/PRJ-medtec_kit/tree/master/installation/)

## Mechanics

### Setup

To complete the kit, one have to 3D print some pieces locate on PRJ-medtec_kit/mecanic/modules. At least we need MDL-motor_support, MDL-rod_fixation and MDL-transducer_support, with these modules we have the stricilly minimum device to make measurement in an acquarium. Use the .stl files present in the different folders for 3d printing them. Note that for the moment MDL-transducer_support will have to be adapted for your own transducer because we have not « serial » transducers to ship with our kit yet. One can do that by using freecad (open the .igs file) modify and then export in .stl file (mesh formats files).

First print MDL-motor_support, at the end it will look to something like that:

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/support_RAW.JPG)

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/support_RAW2.JPG)


Take off the plastique support, there is still plastic in the hole where we will put the motor :

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/support_RAW3_2.JPG)

Take it off too with pliers for example, and it’s finished:


![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/support_evide.JPG)

Now fix the motor to this support with 2 or 4 screw 3 mm diameter, 6mm long.

Now print MDL-rod-fixation, the two holes on each side of this part of the cylinder. The bigger one is for the motor axe. Fix this axis with a 3mm diameter 10 mm long screw. This screw must be 10 mm minimum cause it must stick out so it will hit the motor_support when initialising (searching it's 0). The second one is used to fix the rod, prefer using wood screw 3 mm diameter.

![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/montage1.JPG)


The rod is a metal rod 4 mm diameter, prefer stainless steel, because it will be immersed in water, We use 100 mm long rod, but only limitation on the length is that the transducer must be immersed and the electrical connection of the transducer must not.

Then print the tranducer support and fix it to the rod.


![](https://raw.githubusercontent.com/echopen/echopen_prototyping/master/pictures/7_Mechanic/finish.JPG)


@todo: Comment from jerome2echopen to insert (dont know where) "Update of scheme for motor_control_v3:"



### Arduino code for test

Arduino test code for assembly:

Remarks: 
* If the duration of the pulse is too long (>125 ns) delete line 6 (NOP;), this can happened with "bad" arduino copy.

```
#define NOP asm volatile ("nop\n\t");

void pulse()
{
PORTD=B01010000;
NOP;
PORTD=B00000000;
}

void setup() {
// put your setup code here, to run once:
DDRD = B01010000;
}

void loop() {
// put your main code here, to run repeatedly:
pulse();
delayMicroseconds(500);
}
```
