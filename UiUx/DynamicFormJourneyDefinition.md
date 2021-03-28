#### Dynamic Form Journey Definition

- This pattern assists the other dynanic and custom UI/UX patterns by providing a dynamic way for form creartion and manipulation
  - In this pattern (especially when combined with the use of a reactive development language framework) the whole set of possible
    fields are being rendered on the screen (DOM in Web Applications, Desktop in Applications, etc). 
  - A text based configuration descriptor (JSON, YAML, XML, etc) can then be utilisied to allow one element to automatically
    review previous elements and determine what to display. For example, pull down menu options could be changed depending on
    previous selections that the user has made, components can be deeemed mandatory or hidden/shown based on those past selections,
    component style/stylesheet and colour options may altered, etc.
    - For this to work, a GLOBAL context of some type (in ReactJS, for example, state/config/redux themes can be utilised) or 
      another GLOBALLY or SECTION BASED (e.g. bounded context pattern, master data management specific pattern, etc) memory
      loaded data source may be needed.
     
Example:
```json
[    
    {
        if: [ {"ElementaA": "10"}, {"ElementB": "B"} ],
        then: [ 
                  { key: "27 ", value: "Value 27" },
                { key: "32 ", value: "Value 32" }
              ],         
    },
 { more similar statements }  
]
```

**Combining this pattern with other similar pattern**

- In the case of multiple dynamic patterns (for example Custom Components Patternt combined with Dynamic Component 
  Definition and Explanatory Ui Ux Pattern, etc.) the correct way to execute this PATTERN CHAIN would be:-
    - Define the dynamic components, load the correct values and add them to the application 
      (WEB = DOM, DESKTOP = language specific mechanism, etc)
    - In each Custom Component, validate what values to display when the GLOBAL 
      value store changes (eg in ReactJS useEffect and useState to monitor GLOBAL STATE JSON changes).
    - Add any additional validation when something is being typed into the component 
      (for example in reactJS bounded components, validate on onChange() events and store/change state accordinly)
    - When a change occurs, update the GLOBAL state (for example in ReactJS, the State/Redux/Config elements).
