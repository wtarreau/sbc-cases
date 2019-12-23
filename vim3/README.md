This model is for Khadas's VIM3/VIM3L board.

It covers the total internal height which includes the I/O connector. It also
features a side micro-USB based TTL serial adapter connected to ttyS0. This
module simply needs to be glued on top of the WiFi chip between the two antenna
connectors. All 3 buttons are cut and marked ('P','F','R').

The internal dimensions are:
  W = 82.5 mm
  D = 57 mm
  H = 13.5 mm

This model was made for 2mm thick acrylic, resulting in a total external size
of:
  W = 86.5 mm
  D = 61 mm
  H = 17.5 mm

Respecting the internal I/O connector's height forces one to add one millimeter
on top of the RJ45 connector which is the highest one. This is needed anyway to
allow the tabs of the front panel to stay in place. An extra millimeter was
dded below this connector for the same reason. It might be possible to change
the design to remove the tabs around the RJ45 connector, but this would only
save the bottom millimeter since the I/O connector still requires to add one on
the top side.

The antennas can be glued to the upper side, and there's still enough room
inside to place a small 8mm thick heat sink on top of the SoC, even though this
will have limited effect given that there is no connectivity between the inside
and outside environments.

It should be possible to place an internal 1mm thick aluminum plate to spread
the heat over the whole bottom side's surface and make use of the extra
millimeter added at the bottom.

Two 2mm diameter screws were placed in the rear holes with their nuts in order
to keep the board horizontal inside the box.


Margins of 0.1mm are added around all connectors, thus their locations are off
by 0.1mm and their sizes increased by 0.2mm.
