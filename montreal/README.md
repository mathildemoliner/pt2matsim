# PT2MATSim for Montreal

## Create unmapped transit files for each GTFS folder
For each GTFS, run the class Gtfs2TransitSchedule.java to convert GTFS into MATSim transit_vehicles.xml and transit_schedule.xml
At this point, transit schedule is not mapped on the network.

## Regroup transit files
Before regrouping these files in one, TransitLine id and vehicle Id must be unique, so run renameTransit.ipynb to do.

Run joinTransit.ipynb to group all files in one.

## Map transit files

Run the class PublicTransitMapper.java with java -Xmx8G -cp pt2matsim-22.3-shaded.jar org.matsim.pt2matsim.run.PublicTransitMapper pt_config.xml
to map the transit_schedule on the network.
