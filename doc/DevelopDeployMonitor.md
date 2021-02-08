# Develop, Deploy and Monitor in GCP

## Development

- Cloud Source Repositories: To manage source code the most widely used is Git. Which can be self managed or marketplace service.
GCP provider fully Cloud Source Repositories managed by Google Cloud.  

- Cloud Function: Runtime or on the fly processing of file/data can be used in Cloud Function. Uses JS and runs on Node.js environment. Event are used to trigger the function from the code.

## Deployment

- Deployment Manager: Managing environment or setting up the environment can be done by Shell or Cloud services. It uses `yaml` or `py` template file to configure the services. These template can be versioned and store in Cloud Source Repositories.

## Monitoring

- Stackdriver: To monitor, logging, debug, error reports, trace. Performance and Availbility(healthcheck) can be checked. Uptime checks, Alerts, Notifications, Dashboards, Log metrics & Error and write rule for alerting and notification. Debug will need access to source code without much relying on the logging. 