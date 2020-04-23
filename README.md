# To-do: Please create some sort of 'default expected dictionary' (not defaultdict) for the results.
# WalmartClearanceFinder
Tool to find unmarked clearance items at Walmart stores across the US.

## What does this do?

This program uses a series of private API endpoints on Walmart.com to find unmarked clearance items at walmart stores across the United States.

## Installing Dependencies

``` {.sourceCode .bash}
$ pip install -r requirements.txt
```

## How to use


-i determines the skus to search (leave default for all, takes text files and strings as inputs)

-s determines which store to search (leave default for all)

-a determines if it should only find items in stock (setting -a 1 for in stock only, leave default for everything)

-v Determines how verbose the output is

-o determines the destination of the csv file

-t determines how many threads to use


## Examples

### Search for every item that is in stock at Walmart store #2265

```bash

python searchByStore.py -s 2265 -o 2265.csv -a 1 -v 2

```

### Search for every chromecast in the united states

```bash

python searchByStore.py -i 435188866 -o chromecast.csv -v 2

```

### Pull the full inventory of every walmart store in the united states (in-stock and out of stock) (200,000,000+ items)

```bash

python searchByStore.py -o literallyEverything.csv -v 2

```
