---
title: BCPNFR1 - Complex data types - General
description: Module Specification for the Azure Verified Modules (AVM) program
url: /spec/BCPNFR1
type: default
tags: [
  Class-Resource, # MULTIPLE VALUES: this can be "Class-Resource" AND/OR "Class-Pattern" AND/OR "Class-Utility"
  Class-Pattern, # MULTIPLE VALUES: this can be "Class-Resource" AND/OR "Class-Pattern" AND/OR "Class-Utility"
  Type-NonFunctional, # SINGLE VALUE: this can be "Type-Functional" OR "Type-NonFunctional"
  Category-Inputs/Outputs, # SINGLE VALUE: this can be "Category-Testing" OR "Category-Telemetry" OR "Category-Contribution/Support" OR "Category-Documentation" OR "Category-CodeStyle" OR "Category-Naming/Composition" OR "Category-Inputs/Outputs" OR "Category-Release/Publishing"
  Language-Bicep, # MULTIPLE VALUES: this can be "Language-Bicep" AND/OR "Language-Terraform"
  Severity-MUST, # SINGLE VALUE: this can be "Severity-MUST" OR "Severity-SHOULD" OR "Severity-MAY"
  Persona-Owner, # MULTIPLE VALUES: this can be "Persona-Owner" AND/OR "Persona-Contributor"
  Persona-Contributor, # MULTIPLE VALUES: this can be "Persona-Owner" AND/OR "Persona-Contributor"
  Lifecycle-BAU, # SINGLE VALUE: this can be "Lifecycle-Initial" OR "Lifecycle-BAU" OR "Lifecycle-EOL"
  Validation-TBD # SINGLE VALUE: this can be "Validation-BCP/Manual" OR "Validation-BCP/CI/Informational" OR "Validation-BCP/CI/Enforced"
]
priority: 11010
---

## ID: BCPNFR1 - Category: Inputs - Complex data types - General

To simplify the consumption experience for module consumers when interacting with complex data types input parameters, mainly objects and arrays, the Bicep features of Resource-Derived Types or [User-Defined Types](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/user-defined-data-types) **MUST** be used and declared.

{{% notice style="tip" %}}

User-Defined Types are GA in Bicep as of version v0.21.1, Resource-Derived Types are GA as of version v0.34.1, please ensure you have this version(s) installed as a minimum.

{{% /notice %}}

Resource-Derived Types and User-Defined Types allow intellisense support in supported IDEs (e.g. Visual Studio Code) for complex input parameters using objects and array of objects.

{{% notice style="important" title="v0.x Exemption" %}}

While we allow the release of major versions, starting with v1.0.0, retrofitting Resource-Derived Types and User-Defined Types for all modules will take a considerable amount of time.

Therefore, the addition of these features is currently **NOT** mandated/enforced. However, all modules **MUST** implement Resource-Derived Types and User-Defined Types prior to the release of their v1.0.0 version.

{{% /notice %}}
