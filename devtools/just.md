#tools 
[just](https://github.com/casey/just) is a handy way to save and run project-specific commands.

## Installation
Use any package manager 
```bash
apt install just
```

## How to use:
First we need to create a `justfile`.
```
# Example justfile

#<recipie-name>:
# <command-to-run>

start-fe:
	npm i
	npm run dev

	python main.py
	
build: 
	cc main.c foo.c bar.c -o main 
test: build 
	./test	
# here test depends on build, so when you do `just test`, it'll run the `build` 
# recipie first

# You can also run recipes in a recipe like this.
start:
	just start-fe
	just start-be
```

Then you can use `just <recipe-name>` to run a recipe.

Ref:
[just docs](https://just.systems/man/en/)