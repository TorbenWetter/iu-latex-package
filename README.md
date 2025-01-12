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
| author              | Author name                 | Vorname\~Nachname                        |
| matriculationnumber | Matriculation number        | 123456789                                |
| address             | Author's address            | Straße\~1\\\\12345\~Stadt                |
| supervisor          | Supervisor name             | Prof.\~Dr.\~Vorname\~Nachname            |
| submissiondate      | Submission date             | 31.03.2025                               |

## Citations

The package uses `biblatex` with APA style. Available citation commands include:

- `\cite{key}` - Normal citation
- `\textcite{key}` - Citation as part of the text
- `\parencite{key}` - Citation in parentheses

Place your bibliography file (default: `main.bib`) in your project directory.

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

## Complete Example

Here's a complete example of a thesis document using this package:

```latex
%! Author = Your Name

\documentclass[11pt]{article}

\usepackage[
  bibliographyfile={main.bib},
  graphicsdir={images/},
  logofile={logo.png},
  type={Bachelorarbeit},
  university={Internationale Hochschule Duales Studium},
  degree={Informatik B.\,Sc.},
  title={Titel der Arbeit},
  subtitle={Untertitel der Arbeit},
  author={Vorname~Nachname},
  matriculationnumber={123456789},
  address={Straße~1\\12345~Stadt},
  supervisor={Prof.~Dr.~Vorname~Nachname},
  submissiondate={31.03.2025}
]{iuthesis}

\begin{document}

% Generate the title page.
\makecover

% Generate the table of contents.
\maketoc

% Main content.
\section{Einleitung}
\label{sec:einleitung}

Text.

\clearpage

\section{Theoretische Fundierung}
\label{sec:theoretische-fundierung}

\subsection{Unterkapitel 1}
\label{subsec:unterkapitel-1}

Text.

\subsection{Unterkapitel 2}
\label{subsec:unterkapitel-2}

Text.

\clearpage

% ... more sections ...

\section{Fazit}
\label{sec:fazit}

Text.

\clearpage

% Generate the bibliography.
\makebibliography

% Appendix.
\appendix

\section{Interviewleitfaden}
\label{sec:interviewleitfaden}

Text.

\clearpage

\end{document}
```

This example demonstrates:

- Package setup with all options
- Document structure with sections and subsections
- Usage of labels for cross-referencing
- Proper placement of structural commands (`\makecover`, `\maketoc`, `\makebibliography`)
- Appendix setup
- Page breaks using `\clearpage`

## Development Environment

For an easy setup of a complete LaTeX development environment with this package pre-configured, you can use the [IU LaTeX Dev Container Template](https://github.com/TorbenWetter/iu-latex-container-templates). This template provides:

- Pre-configured VS Code with LaTeX Workshop extension
- Full TeXLive installation
- This package pre-installed
- Sample thesis structure
- Automatic builds and previews

To use it, you'll need VS Code with the Dev Containers extension installed. Then you can create a new repository using this template by referencing:

```
ghcr.io/torbenwetter/iu-latex-container-templates/thesis:latest
```
