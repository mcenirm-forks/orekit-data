This project contains some data files useful for use with the
[Orekit library](http://www.orekit.org/).

In order to use these files, simply download the
[last archive](https://gitlab.orekit.org/orekit/orekit-data/-/archive/master/orekit-data-master.zip)
and unzip it anywhere you want, note the path of the orekit-data-master folder
that will be created and add the following lines at the start of your program:

```java
File orekitData = new File("/path/to/the/folder/orekit-data-master");
DataProvidersManager manager = DataProvidersManager.getInstance();
manager.addProvider(new DirectoryCrawler(orekitData));
```

This zip file contains JPL DE 430 ephemerides from 1990 to 2069, IERS Earth
orientation parameters from 1973 to March 2018 with predicted date to mid 2018
(both IAU-1980 and IAU-2000), configuration data for ITRF versions used in
regular IERS files, UTC-TAI history from 1972 to mid of 2018, Marshall Solar
Activity Futur Estimation from 1999 to May 2018, the Eigen 6S gravity field
and the FES 2004 ocean tides model.
