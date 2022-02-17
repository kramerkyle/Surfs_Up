# Surfs_Up
## Overview
The Surfs Up Project was conducted to provide insight into Waves and Ice Cream's market. This analysis resulted in the provision of summary statistics for the months of June and December.

# Results
## Key Differences Between June and December
- The Count of Observations in June is ~200 higher
- The Mean Temp in June is ~3.5 degrees higher
- The Minimum Temp in June is 8 degrees warmer

# Summary
## High Level Summary
In an unsurprising fashion, the June temperatures were warmer on aggregate than the December data. This held true across each quartile, mins, and maxes. The standard deviation was also larget in December, suggesting that the month's weather is more erratic than that of June.

## Additional Queries
### Precipitation for Each Month
dec_results = session.query(Measurement.prcp).\
filter(extract('month', Measurement.date) == dec_start.month)

jun_results = session.query(Measurement.prcp).\
filter(extract('month', Measurement.date) == jun_start.month)

### Precipitation at the Most Active Site
dec_precip_results = session.query(Measurement.prcp).\
filter(extract('month', Measurement.date) == dec_start.month).\
filter(Measurement.station == 'USC00519281')

jun_precip_results = session.query(Measurement.prcp).\
filter(extract('month', Measurement.date) == jun_start.month).\
filter(Measurement.station == 'USC00519281')
