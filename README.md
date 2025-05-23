# SHACL Import-Export Tests

This repository contains tests for evaluating tools that transform schemas between SHACL and other formats, including XSD, JSON Schema, LinkML, OWL, RDFS, OpenAPI, and more. The goal is to establish a rigorous and consistent methodology for testing schema transformations, ensuring that all aspects of a schema are thoroughly evaluated.

## Methodology

The testing methodology is designed to be systematic and repeatable, covering various schema components and constraints. Each tool will be tested using the same set of examples to ensure comparability. The methodology includes the following steps:

1. **Schema Components to Test**:
   - Constraints (e.g., cardinality, data types, value ranges)
   - Nested objects and hierarchical structures
   - References and links between schema elements
   - Metadata and annotations
   - Complex data types and enumerations

2. **Test Cases**:
   - Create a set of example schemas in each format (XSD, JSON Schema, etc.) that include the components listed above.
   - Define expected outputs for each transformation (e.g., SHACL to XSD, XSD to SHACL).

3. **Tool Evaluation**:
   - For each tool, perform the following transformations:
     - From SHACL to the target format.
     - From the target format to SHACL.
   - Compare the tool's output against the expected results.
   - Document any discrepancies, limitations, or issues encountered.

4. **Documentation**:
   - Record the results of each test in a structured format.
   - Include details about the tool version, configuration, and runtime environment.

## Repository Structure

The repository is organized as follows:

```
shacl-import-export-tests/
│
├── examples/                # Example schemas for testing
│   ├── xsd/                 # Example schemas in XSD format
│   ├── json-schema/         # Example schemas in JSON Schema format
│   ├── linkml/              # Example schemas in LinkML format
│   ├── owl-rdfs/            # Example schemas in OWL and RDFS formats
│   ├── openapi/             # Example schemas in OpenAPI format
│   └── shacl/               # Example schemas in SHACL format
│
├── results/                 # Test results and reports
│   ├── tool1/               # Results for Tool 1
│   ├── tool2/               # Results for Tool 2
│   └── ...
│
├── tools/                   # Tool-specific configurations and scripts
│   ├── tool1/               # Configuration for Tool 1
│   ├── tool2/               # Configuration for Tool 2
│   └── ...
│
└── README.md                # This file
```

## How to Use

1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```

2. Add your example schemas to the `examples/` directory.

3. Configure the tools you want to test in the `tools/` directory.

4. Run the tests using the provided scripts or your own testing framework.

5. Document the results in the `results/` directory.

## Contributing

Contributions are welcome! If you have additional tools, test cases, or improvements to the methodology, please submit a pull request or open an issue.

## License

This repository is licensed under the MIT License. See the `LICENSE` file for details.