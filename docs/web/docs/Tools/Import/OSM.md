---
title: OSM
---

# osmWebWizard.py

This script opens a web browser and allows selecting a geographic region
on a map. It also provides some controls for specifying random traffic
demand for different traffic modes. When clicking the 'Generate'-button,
the simulation network for the selected area is built based on [OSM data](../../Networks/Import/OpenStreetMap.md), random demand is
generated and [sumo-gui](../../sumo-gui.md) is started.

!!! note
    A [usage tutorial is available](../../Tutorials/OSMWebWizard.md).

All files that make up the scenario are created in a subfolder of the
working directory with the current timestamp (i.e.
{{SUMO}}/tools/2021-02-22-10-00-00/). If you edit the network, you can use the
script *build.bat* to rebuild the random demand.

Call:

```
python tools/osmWebWizard.py
```

The script will keep running so you can build multiple scenarios in your
web-browser. Stop the script when you're done to free up the port again.

!!! caution
    The script requires the environment variable *SUMO_HOME* to be set [as explained here](../../Basics/Basic_Computer_Skills.md#additional_environment_variables).


# osmTaxiStop.py

This script import taxi stands from OSM data. Using the option **--type** you can choose which type of element to add in the SUMO network. For example:

```
python tools/import/osm/osmTaxiStop.py --osm-file <osm-file> -n <net-file> --type parkingArea
```

Will add the taxi stands as parkingAreas.
