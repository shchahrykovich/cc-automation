# Task
Apply algorithm below:

flowchart TD
    A(["Start"]) --> n2["List all dirs in the folder and ask user which one to choose?"]
    B["For each screenshot in the selected folder"] --> C["Read the screenshot file"]
    C --> D["Analyze file and find artefacts"]
    D --> E{"Has UI bugs?"}
    E -- Yes --> F@{ label: "Move the screenshot to the 'ui-bugs' folder" }
    F --> G["Create text file with the screenshot file name and add in the content bug description"]
    E -- No --> H{"Has non English texts?"}
    H -- Yes --> I@{ label: "Move the screenshot to the 'translation-bugs' folder" }
    I --> J["Create text file with the screenshot file name and add in the content translation bug description"]
    n2 --> B


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