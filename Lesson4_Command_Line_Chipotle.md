

1. The contents of the chipotle.tsv file is a tab-delimited file. Each row represents a specific item that was purchased in an order that could contain multiple purchased items. The colummns represent the following:

* The order ID of the order that the item was a part of
* The quantity of the item that was purchased
* The name of the item
* A more detailed description of the item, including ingrediants
* The price of the item, in dollars and cents.

```
head chipotle.csv
tail chipotle.csv
```

2. There are 1,835 orders in the file.

```
cut -f1 chipotle.tsv > tempfile.tsv
sort tempfile.tsv | uniq | wc -l
```

3. There are 4,623 lines in the file.

```
wc -l chipotle.tsv
```

4. The chicken burrito is more popular than the steak burrito. Chicken burritos were ordered 553 times vs. 368 orders for the steak burrito.

```
grep "Chicken Burrito" | wc -l
grep "Steak Burrito" | wc -l
```

5. Chicken burritos more often have black beans (282 times) vs. pinto beans (105 times)

```
grep "Chicken Burrito" chipotle.tsv |grep "Pinto Beans" | wc -l
grep "Chicken Burrito" chipotle.tsv |grep "Black Beans" | wc -l
```

6. Files:
Airline_on_time_west_coast.csv
airlines.csv
bank-additional.csv
bikeshare.csv
chipotle.tsv
citibike_feb2014.csv
drinks.csv
drones.csv
hitters.csv
icecream.csv
imdb_1000.csv
mtcars.csv
NBA_players_2015.csv
ozone.csv
rossmann.csv
rt_critics.csv
sms.tsv
stores.csv
syria.csv
tempfile.tsv
time_series_train.csv
titanic.csv
ufo.csv
vehicles_test.csv
vehicles_train.csv
yelp.csv

```
find . *.?sv
```

7. There are approximately 80 occurrences of the word "dictionary" in the class repository.

```
grep -i -r "dictionary" . | wc -l
```
