# EXPERT RULES

This repository contains a set of rules samples that can be directly used with McAfee Endpoint Security, in the Exploit Prevention policy. The rules were classified in different categories considering its main protection purpose. All the rules within the *GENERIC_RULES* folder can be considered as examples for learning.

## Contributing

Pull requests are accepted and have to contain a markdown file for each rule in the pull request with the following fields.

* **Title**: A short and descriptive title for the rule. e.g. *REMOTE FILE EXECUTION PROTECTION RULE*.
* **Description**: A deep description of the purpose of the rule, stuff, and actions that are supposed to be blocked by the use of the rule.
* **Rule TCL**: The rule TCL code that can be directly used in the *ENS Exploit Prevention* policy.  Something like:
```
Rule {
    Process {
        Include Match_Type { -v ... }
        Exclude Match_Type { -v ... }
    }
    Target {
        Match Match_Object {
            Include Match_Type { -v ... }
            Exclude Match_Type { -v ... }
            Include -access ...
        }
    }
}
```
* **Trigger**: Some steps to trigger the rule and verify that it actually works. You can put a reference here to any public and safe tool.
* **Notes**: Here is the place to add some clarifications related to the rule, how it works related to the OS, limitations (if any), references to any documentation that could help to understand it, etc. 
