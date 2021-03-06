===========
Description
===========

The main goal of the X-Ray Project is to provide information
about Xilinx 7-Series FPGA internals. All obtained chip data is stored in
the project's database and is used by the `Architecture Definitions`_ project
to produce a bitstream for the chosen 7-Series FPGA chip.

The database files are generated by the :doc:`fuzzers <../db_dev_process/fuzzers/index>` and are located in the ``database``
directory. Each supported chip architecture has its own set of files, which are located in ``database/<device_arch>/``.
The database can be quite huge, however it consists only of a few file types.
Some of them are common for the whole 7-Series architecture, but some of them are part specific.

.. _Architecture Definitions: https://github.com/SymbiFlow/symbiflow-arch-defs

Files common for whole 7-Series family:

   - ``mask_*``
   - ``ppips_*``
   - ``segbits_*``
   - ``site_type_*``
   - ``tile_type_*``
   - ``timings/*``

The files specific to a given part are located in a separate directory which is named after the FPGA part name i.e *xc7a35tcpg236-1* or *xc7a50tfgg484-1*.

Files specific for the particular FPGA part:

   - ``package_pins.csv``
   - ``part.json``
   - ``part.yaml``
   - ``tileconn.json``
   - ``tilegrid.json``
