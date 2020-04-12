
```
alias infw='influx write -b rick -o ag -p s'
```

### Write Data to Influx

```
cd csv/examples/data/out
Either syntax works for files.
infw @ui.txt
infw -f ui.txt
```

### Query data from Influx

```
influx query '-o=ag' @ex00.txt

And if you set up your environment see further down in this file...

env | grep INFLUX

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

Locally I have a file called .influxenv which looks like this

```
export INFLUX_TOKEN=ieL6P0KeyZ_DKlxGQiv1VSZELOolY8ISSFVqZX8uw5e-eBolJdnlCUiByAVjoZety-EQPTkaAGveKo-aHjK03Q==
export INFLUX_ORG=ag
export INFLUX_BUCKET_NAME=rick
```

To delete a measurement this command works
```
influx delete -p _measurement="ui" --start="2009-01-02T23:00:00Z" --stop="2020-04-12T23:00:00Z"
```
