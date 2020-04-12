
The data input file comes from here.
https://github.com/stormasm/influx-equity/tree/master/csv/examples/data/out

The query file comes from here.
https://github.com/stormasm/flux-examples/tree/master/examples/stocks

The csv directory is a copy of this repo
https://github.com/stormasm/influx-point-lineprotocol

All new rust development on **point.rs** should be done in the original
repo and not here.  This code is here simply to quickly enable running
and testing and updating the data sets with the most recent equity data.
The reason this copy is here is because I did not want to pollute the
original development repo with continual data updates so it is done
here instead.
