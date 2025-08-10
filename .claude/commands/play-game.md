# Task
Apply algorithm below:

flowchart TD
    A(["Start"]) --> n1["Ask user to enter a number"]
    n1 --> E{"if the input number is >1?"}
    E -- No --> H@{ label: "Show to user message box with text 'Small number'" }
    H --> n2(["End"])
    E -- Yes --> F{"if the input number is >2?"}
    F -- No --> n3@{ label: "Show to user message box with text 'Less than 2'" }
    n3 --> n4(["End"])
    F -- Yes --> G{"if the input number is >3?"}
    G -- No --> n5@{ label: "Show to user message box with text 'Less than 3'" }
    n5 --> n6(["End"])
    G -- Yes --> I{"if the input number is >4?"}
    I -- No --> n7@{ label: "Show to user message box with text 'Less than 4'" }
    n7 --> n8(["End"])
    I -- Yes --> J{"if the input number is >5?"}
    J -- No --> n9@{ label: "Show to user message box with text 'Less than 5'" }
    n9 --> n10(["End"])
    J -- Yes --> K{"if the input number is >6?"}
    K -- No --> n11@{ label: "Show to user message box with text 'Less than 6'" }
    n11 --> n12(["End"])
    K -- Yes --> L{"if the input number is >7?"}
    L -- No --> n13@{ label: "Show to user message box with text 'Less than 7'" }
    n13 --> n14(["End"])
    L -- Yes --> M{"if the input number is >8?"}
    M -- No --> n15@{ label: "Show to user message box with text 'Less than 8'" }
    n15 --> n16(["End"])
    M -- Yes --> N{"if the input number is >9?"}
    N -- No --> n17@{ label: "Show to user message box with text 'Less than 9'" }
    n17 --> n18(["End"])
    N -- Yes --> O{"if the input number is >10?"}
    O -- No --> n19@{ label: "Show to user message box with text 'Less than 10'" }
    n19 --> n20(["End"])
    O -- Yes --> n21@{ label: "Show to user message box with text 'Too large'" }
    n21 --> n22(["End"])


# Notes
- If algorithm requires an input from users call osascript

# Osascript usage examples

## Choose from 4 options
osascript -e 'choose from list {"Red", "Green", "Blue", "Yellow"} with prompt "Pick your favorite colors:" with multiple selections allowed'

## Show confirmation box
osascript -e 'display dialog "Continue?" buttons {"Yes", "No"} default button "Yes"'

## Ask user for input
osascript -e 'text returned of (display dialog "Enter your name:" default answer "")'

## Show message box
osascript -e 'display dialog "Hello from osascript!" buttons {"OK"} default button "OK"'