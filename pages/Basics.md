# Basics

This topic comprises approximately 6% of the Standard form of the exam. Questions are
drawn randomly from the following topics and objectives:

## High-level Magento architecture

#### Describe Magento codepools

- **Community:** contains files that have been extended from the core code pool and that can apply to several different instances of Magento. Most extension developers make their changes and additions in this code pool because their extensions can be used by any merchant who installs their extension.
- **Core:** contains the base Magento application. Only Magento core product developers should change files in this code pool. **NEVER EDIT FILES IN THIS POOL**
- **Local:** contains files that have been extended from the core code pool but that will only be used by a specific instance of Magento. The local code pool is used by merchants who want to customize their platforms, but do not want to make their customizations available to the community at large.


#### Describe typical Magento module structure

Files are grouped together based on functionality into modules. The directory structure below is what you will typically see.

```
├── app/code/community/
│   ├── Vendornamespace/
│   |   ├── Modulename/
|   |   |   ├── Block/
|   |   |   ├── controller/
|   |   |   ├── data/
|   |   |   |   └── vendornamespace_modulename_setup/
|   |   |   ├── etc/
|   |   |   ├── Helper/
|   |   |   ├── Model/
|   |   |   ├── sql/
|   |   |   |   └── vendornamespace_modulename_setup/
```
> **Note:** Please keep in mind that case sensitivity **DOES** matter when naming the module directories shown above.

As shown directory structure above module is broken up into the following components:

- **Blocks:** Responsible for preparing data for display in templates.
- **Controllers:** Contain methods called actions which process web server requests that correspond to a specific module.
- **Resource Models:** Provide an access layer to data for the extension.
- **Configuration:** Module-specific XML configuration files that tell the application how the module interacts with it.
- **Helpers:** Auxiliary classes that implement commonly used business logic. Examples: forms, validators, formatters.
- **Model:** Implement business logic.
- **Schema SQL Scripts:** SQL scripts that implement schema changes to a specific module.
- **Data SQL Scripts:** Scripts that manipulate the data for the SQL schema of a module. Pay strict attention to this as different upgrades were added in Magento Enterprise Edition (EE) 1.11 and Magento Community Edition (CE) 1.6.

#### Describe Magento templates and layout files location

#### Describe Magento skin and JavaScript files location

#### Identify and explain the main Magento design areas (adminhtml and frontend)

#### Explain class naming conventions and their relationship with the autoloader

#### Describe methods for resolving module conflicts.

# Credits

[Magento Extension Developers Guide](http://info2.magento.com/rs/magentosoftware/images/Magento-Extension-Developers-Guide-v1.0.pdf)

[Magento Certified Developer Exam Study Guide](http://info2.magento.com/rs/magentosoftware/images/Certification-Study-Guide-MCD-v1.pdf)
