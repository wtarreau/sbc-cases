This model is for Libre Computer's AML-S805X-AC board, also called "La Frite".

It takes care of the total board's height including eMMC module and its screws.
An opening is made on the side close to the "boot" button to add a small TTL to
USB serial adapter that can be glued on top of the DRAM chip without increasing
the board's total height.

The board's positions and references are taken with the USB ports on the left
and the RJ45 port on the right, with the boot button at the bottom. The origin
is then at the bottom left of the PCB. During measurements the Z positions are
measured from below the PCB with positive values towards most connectors (hence
the eMMC has a negative offset). When designing panels, the Z origin is taken
from the lowest point which is the eMMC screw at -3.2mm.

The board itself doesn't stay perfectly flat when placed on a table. Thus
depending on the material used, it may be needed to place a bit of foam under
it close to the IR receiver.

The connectors are prominently placed out of the board and not all aligned. The
RJ45 port and the micro-USB port both stand out by 1.5mm. The HDMI port stands
out by 2.6mm. On the other side the USB ports stand out by 4mm. This means the
model should include the board's length plus 4mm minus the material's thickness.

The PCB's dimensions are 65.30x56.30mm. With all connectors included, the total
length becomes 72.80mm. The length from USB to RJ45 is 71.70mm. It may be a
good approach to only let the HDMI connector slightly stand out, and to use
1.5mm thick material everywhere.

The minimal internal board dimensions are:
  W = 56.30mm
  D = 65.30mm
  H = 13.20mm

With 1.5mm thick material, the external board's dimensions can be:
  W = 56.30 + 2*1.5 = 59.30mm
  D = 71.70mm
  H = 13.20 + 2*1.5 = 16.20mm

This indicates that it's worth working with *virtual* internal dimentions of:
  W = 56.30mm
  D = 68.70mm
  H = 13.20mm

Margins of 0.1mm are added around all connectors, thus their locations are off
by 0.1mm and their sizes increased by 0.2mm.

This implementation was made for 2mm thick material (temporarily cardboard for
this PoC). The front side (USB ports) was printed both with the castellated
contour and with the inner format which were glued together resulting in a 4mm
thick plate nicely covering the prominent USB ports.

No hole was made for the "boot" button whose purpose to date is not very clear.
