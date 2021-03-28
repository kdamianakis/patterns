#### Dynamic Component Definition (using JSON)

- This pattern is normally combined with the custom component pattern for more efficient usage.
  - Allows a JSON (or any other textual configuration mechanism) to define what information, stylesheet, 
    colour or other text, validation scripts, mandatory, regexpressions and other definitions can be 
    read from that file and used to CONFIGURE the CUSTOM UI COMPONENT / ELEMENT.

```json
{
    elementName: "additionalDeclarationType",
    componentId: 1,
    pullDownMenu: [
      { key: "A", value: "A Value." },
      {
        key: "B",
        value: "Another Value.",
      },
    ],
    boxCode: "",
    parenthesisCode: "abc",
    validation: false,
    borderColor: "",
    validationLogic: { .. some validation logic ...},
    textDescription: "A text descritpion for this component",
    isMandatory: true,
    version: 0,
    furtherInformartionLink: "www.addalinkhere.com",
  },
```
