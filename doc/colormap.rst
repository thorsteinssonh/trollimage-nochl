==========
 Colormap
==========

Example usage
=============

A simple example of applying a colormap on data::

    from trollimage.colormap import rdbu
    from trollimage.image import Image

    img = Image(data, mode="L")
    
    rdbu.set_range(-90 + 273.15, 30 + 273.15)
    img.colorize(rdbu)
    
    img.show()

.. image:: _static/hayan_simple.png

A more complex example, with a colormap build from greyscale on one end, and spectral on the other, like this:

.. image:: _static/my_cm.png

::

    from trollimage.colormap import spectral, greys
    from trollimage.image import Image

    img = Image(data, mode="L")
    
    greys.set_range(-40 + 273.15, 30 + 273.15)
    spectral.set_range(-90 + 273.15, -40.00001 + 273.15)
    my_cm = spectral + greys
    img.colorize(my_cm)

    img.show()

.. image:: _static/hayan.png


Now applying a palette to the data, with sharp edges::

    from trollimage.colormap import set3
    from trollimage.image import Image

    img = Image(data, mode="L")
    
    set3.set_range(-90 + 273.15, 30 + 273.15)
    img.palettize(set3)
    
    img.show()

.. image:: _static/phayan.png

API
===

.. automodule:: trollimage.colormap
   :members:
   :undoc-members:

Default Colormaps
=================

Colors from www.ColorBrewer.org by Cynthia A. Brewer, Geography, Pennsylvania State University.

Sequential Colormaps
~~~~~~~~~~~~~~~~~~~~

blues

|pict1|

.. |pict1| image:: _static/blues.png

greens

|pict2|

.. |pict2| image:: _static/greens.png

greys

|pict3|

.. |pict3| image:: _static/greys.png

oranges

|pict4|

.. |pict4| image:: _static/oranges.png

purples

|pict5|

.. |pict5| image:: _static/purples.png

reds

|pict6|

.. |pict6| image:: _static/reds.png

bugn

|pict7|

.. |pict7| image:: _static/bugn.png

bupu

|pict8|

.. |pict8| image:: _static/bupu.png

gnbu

|pict9|

.. |pict9| image:: _static/gnbu.png

orrd

|pict10|

.. |pict10| image:: _static/orrd.png

pubu

|pict11|

.. |pict11| image:: _static/pubu.png

pubugn

|pict12|

.. |pict12| image:: _static/pubugn.png

purd

|pict13|

.. |pict13| image:: _static/purd.png

rdpu

|pict14|

.. |pict14| image:: _static/rdpu.png

ylgn

|pict15|

.. |pict15| image:: _static/ylgn.png

ylgnbu

|pict16|

.. |pict16| image:: _static/ylgnbu.png

ylorbr

|pict17|

.. |pict17| image:: _static/ylorbr.png

ylorrd

|pict18|

.. |pict18| image:: _static/ylorrd.png


Diverging Colormaps
~~~~~~~~~~~~~~~~~~~

brbg

|pict21|

.. |pict21| image:: _static/brbg.png

piyg

|pict22|

.. |pict22| image:: _static/piyg.png

prgn

|pict23|

.. |pict23| image:: _static/prgn.png

puor

|pict24|

.. |pict24| image:: _static/puor.png

rdbu

|pict25|

.. |pict25| image:: _static/rdbu.png

rdgy

|pict26|

.. |pict26| image:: _static/rdgy.png

rdylbu

|pict27|

.. |pict27| image:: _static/rdylbu.png

rdylgn

|pict28|

.. |pict28| image:: _static/rdylgn.png

spectral

|pict29|

.. |pict29| image:: _static/spectral.png

Qualitative Colormaps
~~~~~~~~~~~~~~~~~~~~~

set1

.. image:: _static/palette0.png

set2

.. image:: _static/palette1.png

set3

.. image:: _static/palette2.png

paired

.. image:: _static/palette3.png

accent

.. image:: _static/palette4.png

dark2

.. image:: _static/palette5.png

pastel1

.. image:: _static/palette6.png

pastel2

.. image:: _static/palette7.png


Rainbow Colormap
~~~~~~~~~~~~~~~~

Don't use this one ! See here_ why

.. _here: http://data3.mprog.nl/course/15%20Readings/40%20Reading%204/Borland_Rainbow_Color_Map.pdf

rainbow

|pict30|

.. |pict30| image:: _static/rainbow.png
