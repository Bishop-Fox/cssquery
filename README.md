# __CSSQuery Tool__

`cssquery` is a versatile tool for extracting CSS selector contents or specific property values from a CSS file. It can be used both as a command-line tool and as a module in other Python scripts.

## __Features__

- Extracts all instances of a CSS selector's content.
- Retrieves specific property values within a CSS selector.
- Supports verbose output for detailed debugging information.
- Can be used as a standalone command-line tool or imported as a module.

## __Usage__

### __Command-Line Tool__


```css
    cssquery[-v] /path/to/file.css.selector[.property]
```

- v: Optional flag to enable verbose output, providing detailed information about the file path, CSS query, selector, property, and matches during execution.
- `/path/to/file.css.selector[.property]`: The path to the CSS file followed by the selector and optional property you want to query.


## __Examples__


### __Query a Selector:__

Extract all instances of a selector's content:
```bash
cssquery ../base16-dispatch/theme.css.theme-dark
```
### __Query a Property:__

To retrieve a specific property's value within a selector:

```bash
cssquery ../base16-dispatch/theme.css.theme-dark.--blue
```
### __Verbose Output:__

To enable verbose output for debugging:
```bash
cssquery -v ../base16-dispatch/theme.css.theme-dark.--blue
```
### __*As a Module*__

You can also import the `cssquery` function into another QMarkdown script:
```python
# another_script.qmd
from cssquery import cssquery

file_path = '../base16-dispatch/theme.css'
css_query = 'theme-dark.--blue'
result = cssquery(file_path, css_query, verbose=True)

if result:
    print("Result:", result)
else:
    print("No match found.")
```
### __Requirements__

- Python 3.x

### __Installation__

- Clone the repository or download the `cssquery.qmd` script.
- Ensure you have Python 3.x installed on your system.

### __Contributing__
Contributions are welcome! If you find a bug or have a feature request, please open an issue or submit a pull request.

### __License__

- This project is licensed under the MIT License.
