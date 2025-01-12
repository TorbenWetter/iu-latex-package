# iu-latex-package

A LaTeX Package for Writing Scientific Work at IU International University

## Package Options

| Option              | Description                 | Default Value                            |
| ------------------- | --------------------------- | ---------------------------------------- |
| bibliographyfile    | Path to bibliography file   | main.bib                                 |
| graphicsdir         | Directory containing images | images/                                  |
| logofile            | University logo file name   | logo.png                                 |
| type                | Type of work                | Bachelorarbeit                           |
| university          | University name             | Internationale Hochschule Duales Studium |
| degree              | Degree program              | Informatik B.\\,Sc.                      |
| title               | Thesis title                | Titel der Arbeit                         |
| subtitle            | Thesis subtitle             | Untertitel der Arbeit                    |
| author              | Author name                 | Vorname~Nachname                         |
| matriculationnumber | Matriculation number        | 123456789                                |
| address             | Author's address            | Straße~1\\\\12345~Stadt                  |
| supervisor          | Supervisor name             | Prof.~Dr.~Vorname~Nachname               |
| submissiondate      | Submission date             | 31.03.2025                               |

## Abbreviation Commands

The package provides several convenient commands for common German abbreviations:

- `\zB` - z. B. (zum Beispiel)
- `\dash` - d. h. (das heißt)
- `\usw` - usw. (und so weiter)
- `\etc` - etc.
- `\bzw` - bzw. (beziehungsweise)
- `\ggf` - ggf. (gegebenenfalls)
- `\ua` - u. a. (unter anderem)
- `\oAE` - o. Ä. (oder Ähnliches)
- `\etal` - et al.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Automatic Releases

This package uses GitHub Actions to automatically create new releases when changes are made to the `iuthesis.sty` file. Each release includes the latest version of the package file.
