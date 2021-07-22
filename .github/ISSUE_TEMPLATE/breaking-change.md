name: "ASP.NET Core breaking change"
description: Report a change in ASP.NET Core that breaks something that worked in a previous version. Intended mostly for product-team use.
title: "[Breaking change]: "
labels: "Breaking change"
assignees:
 - gewarren
body:
  - type: textarea
    id: description
    attributes:
      label: Description
      description: Brief description of the breaking change.
    validations:
      required: true
  - type: dropdown
    id: version
    attributes:
      label: Version
      description: What version of .NET introduced the breaking change?
      options:
        - .NET 6 Preview 6
        - .NET 6 Preview 7
        - .NET 6 RC1
        - .NET 6 RC2
        - .NET 6 GA
        - Other (please put exact version in description textbox)
    validations:
      required: true
  - type: textarea
    id: old-behavior
    attributes:
      label: Previous behavior
      description: Describe the previous behavior. Include code snippets if applicable.
    validations:
      required: true
  - type: textarea
    id: new-behavior
    attributes:
      label: New behavior
      description: Describe the new behavior. Include code snippets if applicable.
    validations:
      required: true
  - type: checkboxes
    id: change-type
    attributes:
      label: Type of breaking change
      options:
        - label: Binary incompatible (code must be recompiled to use the newer API version)
        - label: Source incompatible (code must be changed and recompiled to use the newer API version)
    validations:
      required: true
  - type: textarea
    id: reason
    attributes:
      label: Reason for change
      description: Describe why the breaking change was introduced.
    validations:
      required: true
  - type: textarea
    id: recommended-action
    attributes:
      label: Recommended action
      description: Describe the recommended action an affected user should take, such as workarounds or examples of code changes.
    validations:
      required: true
  - type: dropdown
    id: area
    attributes:
      label: Feature area
      description: What feature area(s) does the change affect?
      options:
        - ASP.NET Core (Default)
  - type: textarea
    id: affected-apis
    attributes:
      label: Affected APIs
      description: List all the APIs affected by this change. For methods, clarify if it's all overloads or specific overloads.
      placeholder: None.
    validations:
      required: true
