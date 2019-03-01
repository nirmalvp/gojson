GoJSON is a command line utility to handle json in command line. 

### What it does

[x] Retrieve nested objects
[x] Pretty print JSON
[x] Validate JSON
[x] Aggregate finct


## Installing

With go

```sh
$ go get -u github.com/sarathsp06/gojson
```

Or you may download the binary here [download](https://github.com/sarathsp06/gojson)

#### Key Syntax
* Key is a set of `.` seperated nested keys
* Can use 0-n numbers to refer to index in arrays
 
### Usage Examples

##### Getting a value 

Get a string:
```sh
$ echo '{"name":{"first":"Tom","last":"Smith"}}' | gojson name.last
Smith
```

Get a block of JSON:
```sh
$ echo '{"name":{"first":"Tom","last":"Smith"}}' | gojson name
{"first":"Tom","last":"Smith"}
```

Try to get a non-existent key:
```sh
$ echo '{"name":{"first":"Tom","last":"Smith"}}' | gojson name.middle
null
```

Get an array value by index:
```sh
$ echo '{"friends":["Tom","Jane","Carol"]}' | jj friends.1
Jane
```
