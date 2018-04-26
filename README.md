# EDMX-Label-Build-Runtime

NL for Business
The Netherlands
www.nl4b.com
(c) April, 2018

We build the EDMX Label Builder to solve the gap between S/4HANA automatic generated or non-SAP OData services and the VDM Generator of S/4HANA Cloud SDK. The tool will be able to generate a properties file with can be modified by the user. The tool can be used to check the new properties file for inconsistency and will be used to generate a modified consistent EDMX file for the VDM generator.

arguments:  
-b,--build                     Build edmx file out of template and properties file  
-c,--check                     Check properties files on duplicate labels  
-e,--edmx-file <arg>           The name of the source or generated edmx file  
-g,--generate                  Generate edmx template and properties files  
-h,--help                      Display this help  
-o,--override-files            Flag to override existing files  
-p,--edmx-properties <arg>     The name of the properties file to generate  
-r,--release-info              Show release info  
-t,--edmx-template <arg>       The name of the edmx template file  
-v,--version                   Prints the tool version info  
-x,--extend-properties         Flag to extend an existing properties file  

usage:
1. Generate edmx template and properties file  
   java -jar edmx-sap-label-builder-1.0.4.jar --generate --edmx-file <arg> --edmx-template <arg> --edmx-properties <arg>  
2. Validate edmx template and properties file  
   java -jar edmx-sap-label-builder-1.0.4.jar --check --edmx-template <arg> --edmx-properties <arg>  
3. Build a new edmx file based on template and properties files  
   java -jar edmx-sap-label-builder-1.0.4.jar --build --edmx-file <arg> --edmx-template <arg> --edmx-properties <arg>  


Release Notes:  
Release 1.0.4 - April 25, 2018  
[FIX] Correct typo in argument --override-files  
[FIX] Sort Properties in check procedure after reading property file   

Release 1.0.3 - April 24, 2018  
[FEATURE] Argument for override template and properties file if exists  
[FEATURE] Extend existing properties file with missing properties  
[FIX] Properties in property file sorted  

Release 1.0.2 - April 23, 2018  
[FEATURE] Add sap:labels to template for function imports to include niche name in odata-generator  
[FEATURE] Check sap:labels contains only spaces, numeric and alphanumeric characters.  
[FEATURE] Add release info to application  
[FIX] Add sap:labels to template when sap:labels doesnot exists in entitytype property  
[FIX] Arguments in help in alphabet order  
[FIX] Remove not yet implemented arguments from help  

Release 1.0.1 - April 18, 2018  
[FEATURE] Feature to check properties  
[FEATURE] Check sap:label on empty labels  
[FEATURE] Check duplicate sap:label within an entitytype  
[FIX]     Property in properties file now sorted and grouped on entitytype/property  

Release 1.0.0 - April 16, 2018  
[FEATURE] Generate properties and template file out of edmx file  
[FEATURE] Build new edmx fileout of a properties and template file  

