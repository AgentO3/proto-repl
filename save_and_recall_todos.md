# Save and Recall Feature

## Left to do

### First Version

* Clojure side
  * Allow specifying particular vars to save instead of everything.
  * Document proto repl library
  * Push proto repl library to clojars
* Proto REPL Side
  * Write command to insert save call with keybinding and unique id
  * Write command to display saved values
  * Write command to clear saved values
    * clears code
    * Clears inline display
* Towards end
  * Document the Feature

### Next

* Clojure side
  * Track separate save locations using only the id
  * Keep track of version of saved data per uniq id
* Proto REPL Side
  * Every time the values are fetched and redisplayed the map is collapsed.
    * Need to track the result and then update the view inside it or remember the state of collapsed/not collapsed
  * Send version when fetching.
  * Determine best polling interval (every second)
* Towards end
  * Document the Feature
  * Move gifs to the github cloud cdn instead of in repo

## Future Ideas

### Allow display in a simple table

The `save` call can specify display instructions

```
(save 111 :table)
```

Then the display would show each value in a simple table.