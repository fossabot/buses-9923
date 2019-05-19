*This is a repo for a test assessment, it will be deleted after assessment.*

[![CircleCI](https://circleci.com/gh/tim-hub/buses-9923.svg?style=svg)](https://circleci.com/gh/tim-hub/buses-9923) [![codefactor](https://www.codefactor.io/repository/github/tim-hub/buses-9923/badge?style=flat-square)](https://www.codefactor.io/repository/github/tim-hub/buses-9923)

This is a small NodeJS CLI application. The comments are in **JSDoc** style, can be used to generate documentation easily. **CircleCI** is used as a service for continuous integration during development. **esm** here is used for ECMAScript module loading.



## How to
### Requirements
- yarn
- git


    `yarn` is recommended(`npm` should work too, but it is not used during development)

### Run the app

1. `git clone https://github.com/tim-hub/buses-9923`
2. `cd buses-9923`
2. `yarn`
3. `yarn start r [file path]` absolute or relative path are supported, commands must be separated by lines. for example `yarn start r ./test/data/input/case1.bcmd`
    - `r` stands for read, to read commands from a file, a file path is required here.
4. The output in console will be `0,1,NORTH`

## About Input/Output

### Input
- Input, from a file which contains the commands, sample files are in `test/data/input/`

```
PLACE 1,2,EAST
MOVE
MOVE
LEFT
MOVE
REPORT
```
As the example above, commands are separated by new line.
Currently there are 5 valid commands, `MOVE`, `LEFT`, `RIGHT`, `REPORT` and `PLACE [x],[y],[direction]`, a proper `PLACE` command requires 3 parameters,

- `x` and `y` which both are between 0 to 4, x,y stands for the position of bus will be parked.
- `direction` which is `NORTH`or `EAST` or `SOUTH` or `WEST`


### Output
- Output, standard output (to console by default), samples files are in `test/data/output/`

If run the commands like the example above, the output will be

```
3,3,NORTH
```


## Testing
Mocha and Chai are used as test framework ans assertion library.
- `yarn test` will test all testing.
- `yarn test-cli` will test functionality of cli only.

    all testing data in `test/data/` will be tested.



### Sample Data
Sample data is included, which is stored at `test/data/` folder. Fot the testing purpose, both input commands and expected output are stored in the folder (`input` and `output`). For example,

- `input/case1.bcmd` is the file which includes commands to run
- `output/case1.bout` is the relative file which contains the expected result.






## References
- [Requirements Analyse Results](analyse.md)
