.. only:: html

   |updatedisclaimer|

blast2dem
---------

Description
...........

This tool can turn billions of points with via seamless Delaunay triangulation implemented using streaming into large elevation, intensity, or RGB rasters. For more info see the `blast2dem <http://rapidlasso.com/blast2dem>`_ page and its online `README <http://lastools.org/download/blast2dem_README.txt>`_ file.

Parameters
..........

``verbose`` [boolean]
  Generates more textual control output to the console.
  
  Default: *False*

``open LAStools GUI`` [boolean]
  Starts the GUI of LAStools with pre-populated input files.
  
  Default: *False*
  
``input LAS/LAZ file`` [points]
  The file containing the points to be rastered in LAS/LAZ format.

``filter`` [string]
  Specifies which points to use to construct the temporary TIN that is then rastered.

  Default: *---*

``step size / pixel size`` [number]
  Specifies the size of the cells of the grid the TIN is rastered onto.

  Default: *1.0*

``Attribute`` [string]
  Specifies the attribute that is to be rastered.

  Default: *elevation*

``Product`` [string]
  Specifies how the attribute is to be turned into raster values.

  Default: *actual values*

``use tile bounding box`` [boolean]
  Specifies to limit the rastered area to the tile bounding box (only meaningful for input LAS/LAZ tiles that were created with lastile).
  
  Default: *False*

``additional command line parameter(s)`` [string]
  Specifies other command-line switches not available via this menu but known to the (advanced) LAStools user.

  Default: *---*
  
Outputs
.......

``Output raster file`` [raster]
  Specifies where the output raster is stored. Use image rasters like TIF, PNG, and JPG for false color, gray ramps, and hillshades. Use value rasters like TIF, BIL, IMG, ASC, DTM, FLT, XYZ, and CSV for actual values.

Console usage
.............

::

  processing.runalg('blast2dem', verbose, gui, input, filter, step, attribute, product, use_tile_bb, additional, output)

See also the `blast2dem <http://rapidlasso.com/blast2dem>`_ page and its online `README <http://lastools.org/download/blast2dem_README.txt>`_ file.
