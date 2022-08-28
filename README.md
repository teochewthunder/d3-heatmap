# D3 Heatmap
This builds on the earlier [D3 Bar Chart](https://github.com/teochewthunder/d3-barchart). There is some renaming, because "legend" and "scale" no longer make sense. A Heatmap is essentially a two-dimensional chart, thus the chart has two axes - one for players and one for seasons. The third dimension - statistic type - is changeable via the dashboard dropdown list.

## Layout
Remains largely the same, though some measurements have been slightly altered. Size of chart depends on number of players and number of seasons represented on screen.

## Data
The data is the same. No changes. Code will create appropriate strcture.

## Script procedure
1. Get the stat from the drop-down list ("goals" or "appearances")
2. Using the stat, get the maximum value from `graphData` for that stat.
3. A nested `For` loop to create the chart. Number of rows is the number of seasons, and number of columns is the number of players.
4. The fill color of each square is the value divided by the maximum value from step 2. This should get you a number between 0 and 1. This number will be used in the `rgba()` function as the opacity.
