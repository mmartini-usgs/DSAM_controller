# DSAM_controller

Controller code for the upgraded DSAM analyzer of the Woods Hole Center's gas hydrates facility.

    For John Pohlman and Emile Bergeron.  
	It is an interface to receive button actuation and translate
    button sequences into LED indicator lights and output levels
    to actuate valve and analysis sequences.

This code is C for the arduino ATmega3250

Written by Marinna Martini, 12/22/2016

# DSAM program changes – how to

How to implement a change to the output command set, e.g. changing pinsToSet:

1. Change the 0 and 1’s in the spreadsheet DSAMLookupDefinitions.xlsx

2. Note the value in the Unsigned Word Decimal column for pinsToSet

3. Change the value in the program, these are declared in setPinsOneStep, setPinsDilute1, setPinsDilute2, setPinsStandard or setPinsStartup, depending on the process being controlled.

4. Make sure only one version of the DSAM source code is in the directory before opening the Arduino software (it like to cling to old versions)

5. Compile and verify the code

6. Load to the Arduino 

7. The program automatically runs when loaded.  Use the serial monitor to check what is going on.

