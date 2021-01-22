# Neuro-Symbolic Unificaiton Model
This is an implementation of Neuro-Symbolic Unification Model.

## Data Format

Data for this model is in `nl` format - basically Prolog syntax:

```shell
shell$ head data/nations/nations.nl
exports3(netherlands,uk).
economicaid(usa,israel).
booktranslations(egypt,usa).
officialvisits(israel,uk).
relexports(brazil,uk).
relbooktranslations(india,uk).
conferences(uk,india).
independence(uk,cuba).
reltreaties(egypt,china).
negativebehavior(china,uk).
ngo(usa,poland).
```

- `*.nl` files represent *facts and rules* (example of a rule: `isa(X,Y) :- isa(X,Z), isa(Z,Y)`)

- `*.nlt` files represent *rule templates* (example of a rule template: `#1(X,Y) :- #2(X,Z), #3(Z,Y)`)

```shell
shell$ cat data/nations/nations.nlt
20   #1(X, Y) :- #2(X, Y).

20   #1(X, Y) :- #2(Y, X).

20   #1(X, Y) :-
    #2(X, Z),
    #2(Z, Y).
```

## Running

The main file for running NTP is `neural-symbolic_model.ipynb` which takes the path to a dataset file as argument.

## The institute to construct dataset
* __The AI Lab in Soongsil University__

## Citation
```

```
