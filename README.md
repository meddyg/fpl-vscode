# FHIR Profile Language (FPL) for VS Code

Syntax highlighting support for FHIR Profile Language files in Visual Studio Code.

## Features

- Language registration for .fpl files (language id: fpl)
- Highlighting for FPL keywords such as namespace, profile, extension, abstraction, valueset, codesystem, instance, ruleset, element, extends, bind, fixed, and pattern
- Highlighting for binding strengths: required, preferred, extensible, and example
- Highlighting for declarations after profile-like statements and extends clauses
- Highlighting for common property names before colon fields
- Cardinality highlighting for patterns such as 0..1, 1..1, and 0..*
- Code token highlighting for #code and system#code forms
- FHIR path-like token highlighting before block openings
- Boolean constant highlighting for true and false
- Support for line comments, block comments, strings, and bracket auto-closing

## Requirements

- VS Code 1.90.0 or newer

## Installation

Install from a VSIX package:

1. Build the package:

	npm install
	npx vsce package

2. Install the generated VSIX file:

	code --install-extension <your-vsix-file>.vsix

## Example

The extension highlights syntax in files such as:

```fpl
namespace demo

profile MyPatient extends Patient {
  title: "Patient profile"
  cardinality: 0..1
  must-support: true
  bind: required
  code: loinc#1234-5
}
```

## Known Limitations

- This extension currently focuses on syntax highlighting.
- It does not yet include validation, formatting, diagnostics, or code snippets.

## License

MIT. See LICENSE for full text.