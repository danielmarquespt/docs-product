---
tags: support-Integrations_Extensions; support-Integrations_Extensions-overview
---

# Integrate with a SAP System

OutSystems allows you to fetch or update data in a SAP system and use it in your applications.

## Create a Connection to SAP System in your Application

1. In the Logic tab, open the Integrations folder. 
2. Right-click SAP and select Consume SAP Remote Functions.... A window to configure the SAP connection will be displayed. 
3. Fill in the fields regarding the connection and login parameters of your SAP system. These will be the default credentials of your SAP connection, which can be redefined later. 
4. Test your connection by clicking on the Test Connection button. If your connection fails, you can click on Show error detail to see the error message. 

## Import SAP Remote Functions

After setting the connection to SAP you can now import the SAP functions that you will use in your application:

1. Click on the Choose Functions button. A folder tree view with the remote functions, grouped by business use case and SAP functionality, is displayed. 
2. Pick the SAP functions you want to use. Click on the function name to see its details on the right-hand panel: description, input, and output parameters. 
3. Click Finish. 

## Use SAP Remote Functions in your Application

In the Logic tab, open the Integrations folder and SAP element. OutSystems does the following for you:

* Creates the SAP connection you have configured
* Creates the actions for the remote functions you have selected
* Creates the Structures to hold the parameters

You can now use the newly created actions in your application the same way you use the remaining Server Actions.

### SAP Remote Functions Flow

When a SAP Remote Function is called from your OutSystems application, the following flow is executed:

![](../../../.gitbook/assets/sap_remote_function_flow.png)

1. **OnBeforeConnection\(\):** This callback allows you to implement different SAP authentication methods using the [SAP Extensibility API](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/sap-extensibility-api.md%3E), like Logon Tickets or certificates. 
2. **Connect to SAP & Begin Context:** The connection is established to SAP, using the default credentials if no different authentication is defined, and a context in SAP is started for calling the SAP remote function. 
3. **OnBeforeCall\(\):** This callback allows you to customize the values to be sent to SAP. 
4. **Call SAP Remote Function:** Executes the remote function in the SAP System. 
5. **OnAfterCall\(\):** This callback allows you to customize the values returned by SAP. 
6. **Commit/Rollback & End Context:** The changes executed in the SAP System are committed and the context in SAP is ended. If an error occurs, changes are rolled back. 

To call multiple SAP remote functions and have all changes committed only at the end, use [SAP Stateful Calls](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/sap/execute-sap-stateful-calls.md%3E).

### Authentication

When integrating with SAP, OutSystems uses by default the credentials you have provided when you created the connection to the SAP system. These credentials will be used for all SAP remote functions defined under that SAP connection. If you want to use distinct credentials for specific SAP remote functions, you can create a new connection to consume those functions.

You can also use different credentials using one of the following authentication methods:

* **Configure a different connection by environment:** For each SAP Connection in your module, you can [configure a different connection at runtime](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/sap/configure-a-sap-connection-at-runtime.md%3E), which overrides the default connection; This allows your application to use specific SAP systems in certain environments, without having to change or republish the module.
* **Dynamic Login:** Specify the authentication credentials at runtime through the application logic. All SAP remote functions under the connection will require user credentials. A possible use case is for example when modifying data in the SAP system. To implement dynamic login, select **Add Dynamic Login** from the context menu of the SAP Connection.
* **Custom:** Use [SAP Extensibility API](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/sap-extensibility-api.md%3E) to implement other authentication methods, for example, SAP Logon Tickets or certificates. This method uses the 'OnBeforeConnection\(\)' callback to customize the connection.

