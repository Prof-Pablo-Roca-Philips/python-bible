# Welcome to Python Bible

For full documentation visit [mkdocs.org](https://www.mkdocs.org).


## Code Examples

A Plain code bloks:

```
import yaml

# in some circumstances, the yaml module we imoprted may be from a different version, so we need
# to tread carefully when poking at it here (it may not have the attributes we expect)
if not getattr(yaml, '__with_libyaml__', False):
    from sys import version_info

    exc = ModuleNotFoundError if version_info >= (3, 6) else ImportError
    raise exc("No module named '_yaml'")
else:
    from yaml._yaml import *
    import warnings
```

### Python Code Blocks
``` py title="example.py" linenums="1" hl_lines="2 3"
import yaml

# in some circumstances, the yaml module we imoprted may be from a different version, so we need
# to tread carefully when poking at it here (it may not have the attributes we expect)
if not getattr(yaml, '__with_libyaml__', False):
    from sys import version_info

    exc = ModuleNotFoundError if version_info >= (3, 6) else ImportError
    raise exc("No module named '_yaml'")
else:
    from yaml._yaml import *
    import warnings
```

### Emojis
:smile:

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
