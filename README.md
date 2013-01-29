ruby-map-reduce
===============

Some examples and notes about writing map reduces in ruby to run under Hadoop.

Examples
--------

* [Counting Words](https://github.com/adilsoncarvalho/ruby-map-reduce/tree/master/counting-words) (got from [Big Fast Blog][0])

Things I've learned
-------------------

* Running locally without Apache Hadoop

You can test your maps/reduces on your shell prompt by just piping the source data from the source file to the map, sorting its output before piping it to the reduce.

````
cat my-source-file.txt | ruby map.rb | sort | ruby reduce.rb
````

* The output of a map

Each output of a map must always be on the format `key` `tab` `value` `newline`

    puts "#{key}\t#{value}"

[0]: http://www.bigfastblog.com/map-reduce-with-ruby-using-hadoop#coding-your-map-and-reduce-scripts-in-ruby "Map-Reduce With Ruby Using Hadoop | Big Fast Blog"

