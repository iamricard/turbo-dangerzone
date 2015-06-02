To run each set of slides, go to the terminal
and run

```sh
tslide presentation-file.md

# if that throws an error you're probably missing
# tslide by @dominictarr, do this

npm i tslide -g # you may need sudo
```

You may want to use [mdp](https://github.com/visit1985/mdp) to run
the slides (they will look prettier :D)

```sh
git clone git@github.com:visit1985/mdp.git
cd mdp
make
make install
mdp presentation-file.md
```
