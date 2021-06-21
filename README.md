# Computer-Hardware-and-Organization-CS220

This repo contains lab solutions of `Computer-Hardware-and-Organization-CS220` course for 2020-21-II Semester.



## Setup for Verilog


### Installation on Windows system: 
Download `iverilog-v11-20201123-x64_setup.exe` from http://bleyer.org/icarus/. Run
the downloaded installer. When asked for a folder to install, specify
c:\iverilog (this is the default). Just keep clicking next. At one place,
you will be given options to create a desktop shortcut and add executable
folder(s) to the user `PATH`. Select both and click next. Then click to
install. It will install within one minute. It also bundles gtkwave with
the installation. To check whether the installation works correctly, click
on the `Icarus Verilog icon` created on your desktop and then go to the
samples folder. This folder has several verilog files (hello.vl, lfsr16.v,
sqrt.vl, sqrt-virtex.v) and a QUICK_START instruction file. Open up a command prompt window by typing cmd in the search field of your desktop's bottom menu bar. Type the following commands in the command prompt window.

    cd c:\iverilog\samples
    iverilog -o hello hello.vl
    vvp hello

The first line compiles the verilog program hello.vl and the second line
simulates the generated digital circuit. This should print the following:

`Hello, World`

Next, try to compile and run `lfsr16.v`, which models a state machine that
goes through all five-bit states in a certain order.

    iverilog -o lfsr16 lfsr16.v
    vvp lfsr16

The output should show the visited states in the desired order.
Additionally, it creates a file named lfsr16.vcd. This is the input to
gtkwave to view the waveforms. Invoke gtkwave as follows.

    gtkwave lfsr16.vcd

This will pop up the gtkwave viewer. In the upper left corner box, you
will notice +lfsr16_tb. Click on the + and select dut. This will bring up
a list of signals in the rectangle below. Double-click on clk. This will
show the clock signal in the adjacent big box. Double-click on `dout[4:0]`.
This will show the state machine's output signal.


### Installation on Linux systems: 
Please follow the instructions in this page according to your Linux OS:\
https://iverilog.fandom.com/wiki/Installation_Guide.\
To install gtkwave on ubuntu, just do apt-get install gtkwave. To check your installation,
please see the instructions for checking the installation on Windows as
outlined above. 



## Setup for SPIM
Follow the instructions on this page to download and install SPIM
on your home machine.

http://spimsimulator.sourceforge.net/