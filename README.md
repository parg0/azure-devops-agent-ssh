# Connect to Azure DevOps hosted agent via SSH

Sometimes it's very useful to connect to an agent/runner and check logs or roam around the system.
Github permits connecting to their runners via SSH with the usage of specialized actions, but Azure DevOps does not have this functionality. 
Thanks to Twingate, we now have a workaround.


# Installation

1. **Follow [this tutorial](https://www.twingate.com/docs/quick-start) to create a Twingate account and install twingate client on your local machine.**

2. Copy the code from azure-pipelines.yml and change the strings accordingly.
**<CONNECTOR_SERVICE_COMMAND>** - Bash command you obtain from Twingate once you create a connector. It is used to install the connector on the Azure DevOps agent.
**<PUBLIC_KEY>** - Your public SSH key
**<TIMEOUT_INTERVAL>** - Timeout interval to close pipeline execution
3. Run your pipeline, get the agent IP address from the output and ssh to it.


Thanks to [Twingate](https://twingate.com) for the awesome tool they created. 
If you want to learn more about its capabilities, check Viktor Farcic's [review video](https://www.youtube.com/watch?v=LxkAGgn9Yec).
