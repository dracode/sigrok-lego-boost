# sigrok-lego-boost

This repository contains Python code to add a protocol decoder for LEGO BOOST peripherals to sigrok.  For me, the hardest part of this was getting sigrok working in the first place.  I strongly recommend using the pre-compiled AppImage binaries available; the versions in the standard Debian/Ubuntu repositories are hopelessly out of date.  They offer precompiled binaries for Windows as well, though I have not tested the plugin there.  For another option, the latest Kali release actually has recent sigrok builds that you can install normally via apt.

To use this protocol decoder with <a href="https://sigrok.org/wiki/Protocol_decoders">sigrok</a>, simply copy the "boost" directory contained here to the appropriate plugin directory on your system.  For me on Ubuntu and Kali, this is: $HOME/.local/share/libsigrokdecode/decoders/

Now when you start <a href="https://sigrok.org/wiki/PulseView">PulseView</a> or use the command-line tool <a href="https://sigrok.org/wiki/Sigrok-cli">sigrok-cli</a>, you will have the ability to stack the "boost" decoder atop a UART decoder which will turn the serial codes into intelligible messages about what the sensors and motors are sending back to the LEGO BOOST Hub.

Other projects with related info that you might like:<br>
<a href="http://www.treczoks.net/PoweredUp!%20Documentation.pdf">Herr Treczoks' Powered UP! documentation</a><br>
<a href="https://github.com/JorgePe/BOOSTreveng">Jorge Pereira's BOOST Reverse Engineering writeups</a><br>
<a href="https://github.com/undera/pylgbst">Andrey Pokhilko's Python BOOST library</a><br>

