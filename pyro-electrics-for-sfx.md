# Pyro Electrics for SFX 
## The Only Guide You'll Ever Need
### Who is this for?
If you're an SFX Technician working with pyrotechnics in the Film and TV industry. This document is for you.
If you do electrical firing of pyrotechnics for concerts, sports events, battle simulation or defence training. This document is for you. 
In fact, if you fire any sort of pyrotechnics electrically, this document is for you.

### Why should you listen to me?
I'm an electrical engineer and I'm the owner of [easypyro.com](https:easypyro.com). My company is a manufacturer and supplier of pyrotechnic firing systems to customers around the world. I've been doing this since 2015, so I know a thing or two about the electrical firing of pyrotechnics. I've seen plenty of avoidable mishaps simply due to lack of basic electrical knowledge and understanding in the industry. 

### Why should you read this?
You want a solid understanding of what's going on, so that when you press the fire button you **KNOW** what's going to happen. **There should be no chance involved.** If you read this you **WILL** understand how to avoid embarassing pyro failures and stop potentially dangerous misfires and no-blows.

OK, ready? Lets get into it. 

### Back to basics
You use electricity to initiate ("fire") a pyrotechnic on command. **What is electricity?** It's energy, in the form of a flow of electrons (the little bits that fly around the on the outside of atoms). We need to convert this flow of electrons to heat energy, to bring a substance past it's ignition temperature. 

### So how do we do this?
Inside most pyrotechnics, or included with them, you will find an **igniter** (also called an e-match or **e**lectric **m**atch). Two copper wires go inside the head of the igniter where they are connected by a small wire a few millimetres long (usually made of a metal called nichrome) that glows white hot when enough electricity is passed through it.

This is the "bridge" wire. The small nichrome "bridge" wire is typically encased in a pea sized lump of relatively sensitive pyrotechnic composition (we call this a "pyrogen"). This is then dipped several times in a lacquer to protect it.

This entire assembly is what we use to convert the electrical energy to heat energy and electrically fire the main pyrotechnic charge. When the igniter fires it will look similar to striking a traditional match (remember those?) but may have a more vigerous popping noise.

Check out Wikipedia if you want more info on [electric matches](https://en.wikipedia.org/wiki/Electric_match).

OK, so now you know that you need to push electricity (electrons) through an igniter to heat up the little bridge wire inside it. We're not going to worry about anything downstream of this, because that's outside the scope of this "electrical firing" document.

### But why does the little nichrome wire heat up at all?
OK, now we're getting to the meat on the bone. Buckle up, because understanding this basic stuff will mean you know what you're doing.

The wire heats up because it has **Resistance**. Resistance is simply a measure of how much a material restricts the flow of electricity (electrons) through it. We measure resistance in units called **Ohms**. Remember we said the little bridge wire was made of nichrome? Well, we use nichrome (as opposed to say, copper) for the bridge wire because it's got quite a high resistance. When we push electricity (electrons) through a wire, the more resistance it has, the more it heats up!

So we need to push a minimum amount of electricity through the bridge wire in the igniter to generate enough heat to make it fire. 

This "minimum amount" of electricity is usually specified in the datasheet of the pyrotechnic as the "all-fire" **Current**, measured in **Amps (A)** or **milliAmps (mA)** (100ths of an Amp). This is the Current that the manufacturer says will fire the igniter 100% of the time. Note that the igniter **may** fire at Currents significantly less than the "all-fire" current. 

### What the hell is Current anyway?
Let's take a step back here. Most people don't really understand the electrical terms **Current**, **Voltage** and **Resistance**. Understanding these is **crucial** to being a competent electrical firer.

OK, think of electricity (the flow of electrons in a wire) as **water in a pipe**. 

**Voltage** (measured in Volts, symbol V) is like the water pressure. The more Voltage, the more **pressure** we have to push electrons through a given resistance of wire.

**Current** (measured in Amps, symbol A) is like the water flow rate. The more Current, the more **actual electrons** (energy) we are moving. 

**Resistance** (measured in Ohms, pronounced "oh-mm-s", symbol Ω[^1]) is like how much **restriction** there is to the flow eg. a narrow section of water pipe. The higher the resistance, the harder it is to push electrons through, and the more heat we will generate at this point. 

[^1]: Ω Greek symbol Omega, but don't  worry about it.

So imagine this ... a large diameter pipe (low Resistance) with a low pressure (low Voltage) will still move a lot of water (high Current). You can imagine it glugging out everywhere.

A small diameter pipe (high Resistance) with the same low pressure (low Voltage) will not move anywhere near as much water (low Current). Conversly, the same small diameter pipe (again, high Resistance) with a high pressure (high Voltage) will start to move significantly more water (thus high Current), but if it was a wire it would get very hot!

### Putting it all together

OK, so we know the pyrotechnic manufacturer says we need a certain "all-fire" Current to flow through the igniter and make it fire. A great rule of thumb is to assume you need 2 Amps of Current (remember, Current is the amount of electricity flowing) to ensure 100% reliable ignition. This is quite generous as many manufacturers will specify less, but we like to deal in certainties with SFX. It also makes the maths easy. I'll explain why in a second. 

So we have an igniter that needs 2 Amps of Current, on a wire that's say 20 Metres [^2] long, and our firing system runs from a 12V battery (more on batteries later!).

**Will it fire?** Let's find out. 

[^2]: That's 66 feet for you imperialists.
### A little bit of Ohm's Law

Don't panic! **Ohm's Law** is a simple formula that relates the **Voltage** (think "pressure"), **Current** (think "flow rate") and **Resistance** (think "restriction") of a circuit. We need to use it to do a simple calculation to see if our pyro will fire. 

**Ohm's Law** tells us that **Current** (Amps) = **Voltage** (Volts) ÷ **Resistance** (Ohms)

**Get that?** Current (Amps) is equal to the Voltage (Volts) divided by the Resistance (Ohms). If you can remember this, you're golden. 

We know we need **2 Amps** of Current to flow to fire the igniter with 100% reliability. 
We know we are firing from a **12 Volt** battery. 
So we need to measure the **Circuit Resistance** to complete the equation and calculate how much current will actually flow. You should really do this using a **Blasters Ohm Meter** for maximum safety. 

>**Fun Fact!** This used to be called a Blasters Galvanometer. The word "Galv" still lives on to mean "test a circuit". Some peeople say "Galv it out" meaning to "test the circuit so we know everything is connected".

Let's say we measure the **Circuit Resistance** to be **8 Ohms**. 

**Current** (Amps)   = **Voltage** (Volts) ÷ **Resistance** (Ohms)
= 12 Volts ÷ 8 Ohms
= <font color="red">**1.5 Amps** of Current will flow!</font>


So we might have a problem! We need at least **2 Amps** of current to reliably fire the igniter. 

### So what can we do?
1. Increase the voltage
Let's use a 24 Volt firing system instead of a 12 Volt one, this will double the Current. 
**Current** (Amps)   = **Voltage** (Volts) ÷ **Resistance** (Ohms)
= 24 Volts ÷ 8 Ohms
= **3 Amps** of Current will flow!
2. Decrease cable length
A shorter cable length will mean less Resistance. Suppose we half the cable length and this decreases out circuit resistance by 3 Ohms. 
**Current** (Amps)   = **Voltage** (Volts) ÷ **Resistance** (Ohms)
= 24 Volts ÷ 5 Ohms
= **4.8 Amps** of Current will flow!

-- Increase the Voltage.

> ⚠️ **Warning:** Do not push the big red button.

For a given resistance of circuit, you need a certain voltage to push enough current through the igniter to make it work. 

### Types of Firing System

### But my Solenoids!!!

### Not all firing wires are created equal.

Thick vs Thin

Standed vs Solid Core

Copper vs CCA

### MYTH 1 - Bigger is Better!










The current is the **actual amount of water flowing**. For example, a 1 metre (that's 3.3 ft for you Yanks) diameter pipe can have water at a very low pressure (voltage), but still transport a load of water (energy). A 1cm (3/8 inch!) diameter pipe at the same pressure can carry much less water. 

