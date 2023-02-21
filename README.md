# Chase Coppersmith Data Analytics Portfolio
Different personal analytics projects I've created

## Creating a Bitcoin Price Model using various public datasets
The goal here is to evaluate a wide variety of different publicly available market metrics and examine which (if any) can be used to model the future price
of Bitcoin. I wanted to test as many metrics as possible and also used lagged versions and rolling averages of these metrics to create as many potential 
model features as possible and get a feel for which metrics matter most.

This code performs a number of different taks to convert various raw data sources into one big data frame, which is then used to model Bitcoin price over
various time frames. These tasks are briefly outlined below:
**-Read in the data from various sources.
- Format data into useable format. Correct date column formats, re-format and rename columns, aggregate where needed, remove missing values.
- Join data togther based on primary key (date).
- Create lagged versions of each numeric column in data frame
