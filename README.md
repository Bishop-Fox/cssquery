# cssquery

A command-line tool to query CSS files for specific selectors and their content.

## Usage

```sh

python cssquery.py [-v] <file_path> <selector1> <selector2> ...

```

- file_path: The path to the CSS file.
- selector1, selector2, ...: The selectors to match (e.g.,".theme-dark", ".background-primary").
- -v: Optional verbose flag to print additional debugging information.

## Example

python cssquery.py -v theme.css .theme-dark .background-primary

    This will print out the CSS rules that match the .theme-dark and .background-primary selectors in the theme.css file, along with additional debugging information due to the -v flag.

## Installation

Clone the repository: git clone https://github.com/your-username/cssquery.git
Navigate to the repository directory: cd cssquery
Run the script: python cssquery.py [-v] <file_path> <selector1> <selector2> ...

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

MIT
