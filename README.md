# Neuro-Symbolic Unificaiton Model
This is an implementation of Neuro-Symbolic Unification Model.

## Data Format

Data for this model is in `nl` format - basically Prolog syntax:

```shell
shell$ head data/countries/countries.nl
locatedIn(palau,micronesia).
locatedIn(palau,oceania).
locatedIn(maldives,southern_asia).
locatedIn(maldives,asia).
locatedIn(brunei,south-eastern_asia).
locatedIn(brunei,asia).
neighborOf(brunei,malaysia).
locatedIn(japan,eastern_asia).
locatedIn(japan,asia).
locatedIn(netherlands,western_europe).
```

- `*.nl` files represent *facts and rules* (example of a rule: `isa(X,Y) :- isa(X,Z), isa(Z,Y)`)

- `*.nlt` files represent *rule templates* (example of a rule template: `#1(X,Y) :- #2(X,Z), #3(Z,Y)`)

```shell
shell$ cat data/ntp/simpsons.nlt
5   #1(X, Y) :- #2(X, Y).

5   #1(X, Y) :- #1(Y, X).

5   #1(X, Y) :-
    #2(X, Z),
    #2(Z, Y).
```

## Running

The main file for running NTP is `neural-symbolic_model.ipynb` which takes the path to a configuration file as argument.

## The institute to construct dataset
* __The AI Lab in Soongsil University__

## Citation
```

```
