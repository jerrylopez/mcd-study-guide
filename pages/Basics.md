# Basics

This topic comprises approximately 6% of the Standard form of the exam. Questions are
drawn randomly from the following topics and objectives:

## High-level Magento architecture

### Describe Magento codepools

- **Community:** contains files that have been extended from the core code pool and that can apply to several different instances of Magento. Most extension developers make their changes and additions in this code pool because their extensions can be used by any merchant who installs their extension.
- **Core:** contains the base Magento application. Only Magento core product developers should change files in this code pool. **NEVER EDIT FILES IN THIS POOL**
- **Local:** contains files that have been extended from the core code pool but that will only be used by a specific instance of Magento. The local code pool is used by merchants who want to customize their platforms, but do not want to make their customizations available to the community at large.


### Describe typical Magento module structure

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

### Describe Magento templates and layout files location

- **Templates:** `app/design/frontend/THEME_PACKAGE/THEME/template/`
- **Layouts:** `app/design/frontend/THEME_PACKAGE/THEME/layout/`

### Describe Magento skin and JavaScript files location

- **Skin:** `skin/frontend/THEME_PACKAGE/THEME/`
- **JavaScript:** `js/`

### Identify and explain the main Magento design areas (adminhtml and frontend)

### Explain class naming conventions and their relationship with the autoloader

### Describe methods for resolving module conflicts.

To verify your understanding of these objectives, ask yourself the following questions:


1. **How does the framework interact with the various codepools?**
2. **What constitutes a namespace and a module?**
3. **What does the structure of a complete theme look like?**


These code references can be used as an entry point to find answers to the questions above:

- Mage_Core_Model_App
- Mage_Core_Model_Config
- Varien_Autoload

## Magento Configuration

- Explain how Magento loads and manipulates configuration information ○ Describe class group configuration and use in factory methods
- Describe the process and configuration of class overrides in Magento
- Register an Observer
- Identify the function and proper use of automatically available events, including *_load_after, etc.
- Set up a cron job

Since Magento is an XML DOM configuration-based framework, a thorough understanding of how Magento loads and assembles its configuration XML DOM is a core competency.

1. **How does the framework discover active modules and their configuration?**
2. **What are the common methods with which the framework accesses its configuration values and areas?**
3. **How are per-store configuration values established in the XML DOM?**
4. **By what process do the factory methods and autoloader enable class instantiation?**
5. **Which class types have configured prefixes, and how does this relate to class overrides?**
6. **Which class types and files have explicit paths?**
7. **What configuration parameters are available for event observers?**
8. **What are the interface and configuration options for automatically fired events?**
9. **What is the structure of event observers, and how are properties accessed therein?**
10. **What configuration parameters are available for cron jobs?**

These code references can be used as an entry point to find answers to the questions above:

- Mage_Core_Model_App_Area 
- Mage_Core_Model_Config
- Mage_Core_Model_Store
- Varien_Event_Observer

## Internationalization

### Describe how to plan for internationalization of a Magento site
### Describe the use of Magento translate classes and translate files
### Describe the advantages and disadvantages of using subdomains and subdirectories in internationalization

To verify your understanding of these objectives, ask yourself the following questions:

1. **Which method is used for translating strings, and on which types of objects is it generally available?**
2. **In what way does the developer mode influence how Magento handles translations?**
3. **How many options exist to add a custom translation for any given string?**
4. **What is the priority of translation options?**
5. **How are translation conflicts (when two modules translate the same string) processed by Magento?**

These code references can be used as an entry point to find answers to the questions above:

- Mage_Core_Model_Translate::init()
- Mage_Core_Model_Locale::emulate()

# Credits

[Magento Extension Developers Guide](http://info2.magento.com/rs/magentosoftware/images/Magento-Extension-Developers-Guide-v1.0.pdf)

[Magento Certified Developer Exam Study Guide](http://info2.magento.com/rs/magentosoftware/images/Certification-Study-Guide-MCD-v1.pdf)

[Resolving Magento Extension Conflicts by WebShopApps](http://webshopapps.com/blog/2010/11/resolving-magento-extension-conflicts/)

[Ways to Identify and Resolve Magento Extension Conflicts by M-Connect Solutions](https://www.mconnectmedia.com/blog/ways-to-identify-and-resolve-magento-extension-conflicts/)
