
### Write Data to Influx

```
cd csv/examples/data/out
Either syntax works for files.
influx write @ui.txt
influx write -f ui.txt
```

### Query data from Influx

```
influx query '-o=ag' @ex00.txt

And if you set up your environment this way....

env | grep INFLUX
export INFLUX_ORG=ag

cd query
Either syntax works for files
influx query @ex00.txt
influx query -f ex00.txt
```

ex00.txt is the 200 day moving average...

The data input file comes from
[here.](https://github.com/stormasm/influx-equity/tree/master/csv/examples/data/out)

The query file comes from
[here.](https://github.com/stormasm/flux-examples/tree/master/examples/stocks)

The csv directory is a copy of this
[repo.](https://github.com/stormasm/influx-point-lineprotocol)

All new rust development on **point.rs** should be done in the original
repo and not here.  This code is here simply to quickly enable running
and testing and updating the data sets with the most recent equity data.
The reason this copy is here is because I did not want to pollute the
original development repo with continual data updates so it is done
here instead.
