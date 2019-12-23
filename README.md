# Laser-Cut Enclosures for Single Board Computers (SBC)

This project proposes models of lasercut enclosures for various modern SBCs.
Some of them are provided for a given thickness, others are split between
multiple layers which allow one to re-define variations without affecting
the holes locations that can be adjusted at the last moment.

## Examples of realizations

The enclosures below were made on an [EleksMaker A3 Pro laser engraver](https://wtarreau.blogspot.com/2019/09/my-first-experiments-with-eleksmaker-a3.html).

[Khadas VIM3/VIM3L](https://docs.khadas.com/vim3/index.html):

![Khadas VIM3/VIM3L](vim3/vim3-assembled.jpg?raw=true)
[FriendlyELEC NanoPi Fire3](https://www.friendlyarm.com/index.php?route=product/product&path=69&product_id=206):

![FriendlyELEC NanoPi-Fire3](nanopi-fire3/assembled.jpg?raw=true)

[SolidRun Clearfog Base](https://www.solid-run.com/marvell-armada-family/clearfog/):

![SolidRun Clearfog-Base](clearfog-base/assembled.jpg?raw=true)

[Libre Computer AML-S80X-AC ("La Frite")](https://libre.computer/products/boards/aml-s805x-ac/):

![Libre Computer AML-S805X-AC - La Frite](aml-s805x-ac/plugged.jpg?raw=true)

## Contributing

The project must be organized with one directory per board name. Please
be as specific as possible regarding the naming to avoid any later
confusion. Also it's fine if multiple boards share the same model. A
README file should be placed in each directory to mention the specifics
of the model, material type and thickness, presence or not of extra ports,
possibly missing ports.

For submissions, the preferred format is Inkscape's SVG with multiple
layers:
  - one for the front panel with its holes and a bounding box around these
    holes which corresponds to the internal enclosure dimension. This one
    will allow centering when rebuilding the enclosure. If there are holes
    on multiple sides, either use multiple layers with self-explanatory
    names or place them on the same layer.

  - one layer for possible engraving, ideally one per different depth. For
    example one layer may be used to engrave port names and another one to
    enlarge holes around micro-USB connectors.

  - one for optional text and descriptions, dimensions or suggestions

  - one or multiple for the various sides resulting from the lasercut box
    rendering

  - an optional one for the assembled work that eases immediate generation
    for the end users

It is absolutely mandatory that origins used by engraving, holes and
castellated sides are the same, so that one can emit a few GCODE files
and concatenate them to engrave and cut each side without having to move
anything in the setup.

The right way to proceed with these layers now is to stack the holes layer
with their respective sides, using the bounding box for perfect alignment,
then removing this bounding box, then verifying alignment with engraving
layers. Engraving layers must be emitted first. Then the holes must be
emitted, then the external cut. This makes sure that pieces do not move
during all the process.

Given that it is reasonably easy to adjust GCODE output, if an enclosure
is produced for common materials (e.g. 3mm thick acrylic), it can be very
convenient for end users to also provide the GCODE output. Be careful
however that this will rarely work if some engraving layer is present.
