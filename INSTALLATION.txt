BAMBI - BAMBU LAB P1S DASHBOARD
PUBLIC UNRAID INSTALLATION GUIDE
================================

Bambi provides a web dashboard for controlling a
Bambu Lab P1S printer.

REQUIREMENTS
------------
- Unraid with Docker enabled
- Bambu Lab P1S connected to the same network
- Printer IP address
- Printer serial number
- Printer LAN access code
- A private Bambi print token

GETTING YOUR PRINTER IP ADDRESS
-------------------------------
On the P1S touchscreen, open the network/WLAN
settings and locate the IP address.

You can also find the printer in your router's
connected-device list.

GETTING YOUR PRINTER SERIAL NUMBER
----------------------------------
Open the printer's device information screen
or check the serial number printed on its label.

GETTING YOUR PRINTER ACCESS CODE
--------------------------------
Open the printer's network/WLAN settings.

Locate the LAN access code.

This is not your Bambu account password.

Keep this code private.

Do not enable LAN Only Mode just to retrieve
the code. Bambi preserves the printer's
existing Cloud Mode configuration.

CREATING YOUR BAMBI PRINT TOKEN
-------------------------------
Open an Unraid terminal and run:

openssl rand -hex 32

Copy the generated token.

Keep it private. Do not post it in support logs.

UNRAID CONFIGURATION
--------------------

BAMBU_IP
  Enter the printer's local IP address.

BAMBU_SERIAL
  Enter the printer's serial number.

BAMBU_ACCESS_CODE
  Enter the printer's LAN access code.

BAMBU_USERNAME
  Enter bblp.

BAMBI_PRINT_TOKEN
  Enter the random token you generated.

BAMBI_TEST_ACCESS_CODE
  Enter the same printer LAN access code
  used for BAMBU_ACCESS_CODE.

DEFAULT WEB PORT
----------------
6060 on the Unraid server.

SECURITY
--------
Do not share your printer access code or
Bambi print token.

Do not expose Bambi directly to the internet.

PUBLIC IMAGE
------------
The Docker Hub image address will be supplied
when the release is published.

The Unraid Community Applications template
will be prepared for that published image.
