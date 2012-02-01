What is this?
=============

It lets you use PS/2 drivers on modern systems.

This is [tgwbd's ACPIPS2Nub](http://tgwbd.org/darwin/extensions.html),
except it:

* builds correctly on modern 64-bit systems
* does not require a PS/2 mouse for your PS/2 keyboard to work :p

More details
------------

PS/2 drivers expect to see a ps2controller, and to use predefined
interrupts. Neither of these hold on ACPI-based systems.

This:

* finds the PS/2 devices from PNP identifiers
* provides a fake ps2controller device that maps the legacy interrupts.
