---
summary: >-
  Use the logging features of OutSystems, adjusting the logging level of SOAP
  web services if necessary, to troubleshoot SOAP web wervices.
tags: support-application_development; support-Integrations_Extensions
---

# Troubleshoot SOAP Web Services

OutSystems keeps track of all requests and responses of both exposed and consumed SOAP Web Services in your application. These log entries can be viewed in the OutSystems environment management console \(Service Center\).

You can configure the detail level of the logs that OutSystems keeps for each consumed SOAP Web Service, for example increasing the logging level of a given SOAP web service while troubleshooting an issue.

## View SOAP Web Service Logs

To access the logs of your SOAP Web Services, do the following:

1. Go to the management console \(Service Center\) of your OutSystems environment.
2. Go to Monitoring section and select Integrations.
3. In Type, filter the logging you want to see: `SOAP (Consume)` or `SOAP (Expose)`.
4. Click Filter.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/soap/images/integrations-log-screen.png%3E)

## Set Logging Level

You can customize the logging level of a **consumed** SOAP web service of a given module to adjust the amount of stored information about requests/responses.

To configure the logging level of your consumed SOAP Web Service, do the following:

1. Go to the environment management console \(Service Center\) of your OutSystems environment.
2. Go to Factory tab and click on the link with the name of your application.
3. In the Modules tab click on the link with the module name that contains the consumed SOAP Web Service that you want to configure.
4. In the Integrations tab click on the desired consumed SOAP Web Service link to configure it.
5. Set the Logging Level to the desired value: `Default`, `Troubleshoot` or `Full` and click Apply.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/soap/images/log-level-set.png%3E)

## Logging Levels

The available logging levels for consumed SOAP Web Services are the following:

Default : Information is only logged for requests with errors.  
Click on the "Error" link displayed on the right to get more details about the error.

```text
Example:

![](<images/log-level-default.png>)
```

Troubleshoot  
: Information is only logged for requests with errors, along with additional HTTP trace information.  
Click on the "Error" link displayed on the right to get more details about the error.

```text
Example:

![](<images/log-level-troubleshoot.png>)
```

Full : All requests/responses are logged, including additional HTTP trace information.  
Click on the displayed "Error" link or, if there's no error, click on the "Detail" link to obtain detailed logging information.

```text
Example:

![](<images/log-level-full.png>)
```

Take into account that increasing the logging level implies that:

* More information is logged, increasing the amount of information stored in the environment’s database.
* Input and output parameters values are logged along with the request, thus making any sensitive information present in these parameters available through the environment management console.

