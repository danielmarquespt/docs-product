# Supported Configurations for Import Actions from .Net Assembly

The following table lists supported configurations and limitations for the "Import Actions from .Net Assembly" wizard in the current Integration Studio version.

For the supported assembly versions please check the [System Requirements](https://success.outsystems.com/Support/Enterprise_Customers/Installation/OutSystems_Platform_system_requirements>).

|  Import Actions from .Net Assembly |  |
| :--- | :--- |
|  \*\*Imported Elements\*\* |  – Non-Abstract Public Methods \(Static or Instance\)  – Non-Abstract Public Properties \(Static or Instance\)  – Public Fields \(Static or Instance\)  – Public Instance Constructors  – Web Service Methods |
|  \*\*Limitations\*\* |  – Cannot import Index Properties  – Cannot import Delegate Types  – Cannot import Structures  – Cannot import Enumerations  – Cannot import Generic Methods \(although Generic Types are supported in its parameters and return value\)  – Members of Generic Classes and of their inner classes are not imported  – Only static Members of Abstract Classes can be imported |

