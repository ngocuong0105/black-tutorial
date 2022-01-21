## Black tutorial

"Black is the uncompromising Python code formatter."

- Black doesn’t reformat blocks that start with ```# fmt: off``` and end with ```# fmt: on```, or lines that ends with ```# fmt: skip```. ```# fmt: on/off``` have to be on the same level of indentation.

- Check black coding style [here](https://black.readthedocs.io/en/stable/the_black_code_style/current_style.html). 

### Configuration via a file
Black is able to read project-specific default values for its command line options from a pyproject.toml file. You can also explicitly specify the path to a particular file that you want with ```--config```. In this situation Black will not look for any other file.


## Commands
Run black on particular file:
```
black tutorial.py
```

Passing --check will make Black exit with:
- code 0 if nothing would change;
- code 1 if some files would be reformatted; or
- code 123 if there was an internal error
```
black test.py --check
```

Passing --diff will make Black print out diffs that indicate what changes Black would’ve made.
```
black test.py --diff
```

Run black in CLI:
```
echo "print ( 'hello, world' )" | black -
```

Run all *.py files in curent directory:
```
black .
```

## Questions

Do you have a pyproject.toml config file for black or you use the default.

How can I run multiple files within black?