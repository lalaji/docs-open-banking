WSO2 Open Banking Accelerator is a technology stack catered to speed up the implementation of an open banking solution. 
You can use the WSO2 Open Banking Accelerator on top of the WSO2 Identity Server and API Manager to obtain an environment 
for Identity Access Management and API management in open banking. 

This section guides you on how to set up the solution in a local environment. Follow the instructions to find how you 
can quickly set up and try out a basic flow.

!!! tip "Prerequisites"
    1. Download Open Java Development Kit (OpenJDK) version 11 or 17 to the local environment based on the base product versions you use.

        !!!info
            See [Compatibility](../install-and-setup/prerequisites.md#compatibility) for compatible JDK versions.

    2. In the environment variables, update the JAVA_HOME and PATH variables. For instance, you can do this on a Mac/Linux server by adding the following to the ~/.bashrc file:
        ```
        export JAVA_HOME="<JDK_LOCATION>"
        export PATH=$PATH:$JAVA_HOME/bin
        ```
    
    3. Setup a database server using any of the following:
         - MySQL 8.0
         - Oracle 19c
         - Microsoft SQL Server 2017
         - PostgreSQL 13
         
        !!!info
            See [Compatibility](../install-and-setup/prerequisites.md#compatibility) if you are using MySQL 8.0.

        !!!note
            We do not recommend configuring H2 database in the production environment.
    
## Installing base products

1. Download and extract the required base products. You can use any of the following combinations:

    <table>
      <tr>
        <th></th>
        <th>WSO2 Identity Server</th>
        <th>WSO2 API Manager</th>
        <th>WSO2 Streaming Integrator</th>
      </tr>
    <tbody>
      <tr>
        <th>Combination 01</th>
        <td><a href="https://wso2.com/identity-and-access-management/previous-releases/">5.11.0</a></td>
        <td><a href="https://wso2.com/api-management/previous-releases/">4.1.0</a> or <a href="https://wso2.com/api-management/previous-releases/">4.0.0</a></td>
        <td><a href="https://wso2.com/streaming-integrator/previous-releases/">4.1.0</a> or <a href="https://wso2.com/streaming-integrator/previous-releases/">4.0.0</a></td>
      </tr>
      <tr>
        <th>Combination 02<br></th>
        <td><a href="https://wso2.com/identity-and-access-management/previous-releases/">6.0.0</a></td>
        <td><a href="https://wso2.com/api-manager/">4.2.0</a></td>
        <td><a href="https://wso2.com/streaming-integrator/">4.2.0</a></td>
      </tr>
      <tr>
        <th>Combination 03<br></th>
        <td><a href="https://wso2.com/identity-and-access-management/previous-releases/">6.1.0</a></td>
        <td><a href="https://wso2.com/api-manager/">4.2.0</a></td>
        <td><a href="https://wso2.com/streaming-integrator/">4.2.0</a></td>
      </tr>
    </tbody>
    </table>
 
2. To configure the Identity Server with the API Manager, download the respective WSO2 IS Connector according to the API Manager version you have downloaded. 

    - [WSO2 IS Connector for API Manager 4.2.0](https://apim.docs.wso2.com/en/4.2.0/assets/attachments/administer/wso2is-extensions-1.6.8.zip)
    - [WSO2 IS Connector for API Manager 4.1.0](https://apim.docs.wso2.com/en/4.1.0/assets/attachments/administer/wso2is-extensions-1.4.2.zip)
    - [WSO2 IS Connector for API Manager 4.0.0](https://apim.docs.wso2.com/en/4.0.0/assets/attachments/administer/wso2is-extensions-1.2.10.zip)

## Installing WSO2 Open Banking Accelerator

1. Download and extract the latest Open Banking Accelerator 3.0 version. 

    - Current latest version [3.3.0](https://github.com/wso2/financial-services-accelerator/releases/tag/v3.3.0).
              
2. WSO2 Open Banking Accelerator contains the following accelerators:
   
    - wso2-obiam-accelerator-3.x.0
    - wso2-obam-accelerator-3.x.0
    - wso2-obbi-accelerator-3.x.0
            
3. This document uses the following placeholders to refer to the following products:
        
    | Product | Placeholder |
    |---------|---------    |
    |WSO2 Identity Server|`<IS_HOME>`|
    |WSO2 API Manager|`<APIM_HOME>`|
    |WSO2 Open Banking Identity Server Accelerator|`<OB_IS_ACCELERATOR_HOME>`|
    |WSO2 Open Banking API Manager Accelerator |`<OB_APIM_ACCELERATOR_HOME>`|
    |WSO2 IS Connector for API Manager |`<IS_EXTENSION>`|

## Getting WSO2 Updates

The WSO2 Update tool delivers hotfixes and updates seamlessly on top of products as WSO2 Updates. They include 
improvements that are released by WSO2. You need to update the base products and accelerators using the relevant script.

1. Go to `<PRODUCT_HOME>/bin` and run the WSO2 Update tool:

    - Repeat this step for the WSO2 Identity Server, API Manager, and Stream Integrator products.
    
        ```bash tab='On Linux'
        ./wso2update_linux 
        ```
        
        ```bash tab='On Mac'
        ./wso2update_darwin
        ```
        
        ```bash tab='On Windows'
        ./wso2update_windows.exe
        ```

2. Go to `<ACCELERATOR_HOME>/bin` and run the WSO2 Update tool:

    - Repeat this step for the WSO2 Open Banking Identity Server, API Manager, and Business Intelligence accelerators.

        ```bash tab='On Linux'
        ./wso2update_linux 
        ```
        
        ```bash tab='On Mac'
        ./wso2update_darwin
        ```
        
        ```bash tab='On Windows'
        ./wso2update_windows.exe
        ```
   
For more information, see the [WSO2 Updates documentation](https://updates.docs.wso2.com/en/latest/updates/overview/).
