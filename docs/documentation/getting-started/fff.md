---
title: fff
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

# Deploy JFrog Worker

> Description:
> Description: Learn how to deploy and update JFrog worker definitions on your Artifactory instance using the CLI command with various configuration options.
> This command is used to update the worker definition (code, description , filter, secret ...) on your Artifactory instance.
> This command is used to update the worker definition (code, description, filter, secret, etc.) on your Artifactory instance.

<Cards columns="2">
  <Card title="Command Name" icon="terminal">
    `worker deploy` or `worker d` (abbreviation)
  </Card>

  <Card title="Default Timeout" icon="clock">
    5000 milliseconds (5 seconds)
  </Card>
</Cards>

<Accordion title="Command Parameters" icon="cogs">
  | Parameter            | Command / Description                                      |
  | -------------------- | ---------------------------------------------------------- |
  | Command name         | worker deploy                                              |
  | Abbreviation         | worker d                                                   |
  | **Command options:** |                                                            |
  | `--server-id`        | \[Optional] Server ID configured using the config command. |
  | `--timeout-ms`       | \[Default: 5000] The request timeout in milliseconds.      |
  | `--no-secrets`       | \[Default: false] Do not use registered secrets.           |

  | Parameter      | Description                                                |
  | -------------- | ---------------------------------------------------------- |
  | `--server-id`  | \[Optional] Server ID configured using the config command. |
  | `--timeout-ms` | \[Default: 5000] The request timeout in milliseconds.      |
  | `--no-secrets` | \[Default: false] Do not use registered secrets.           |
</Accordion>

<Tabs>
  <Tab title="Basic Usage">
    Deploy a worker to server with default settings:

    ```bash
    jf worker deploy
    ```
  </Tab>

  <Tab title="With Server ID">
    Deploy a worker to a specific server configuration:

    ```bash
    jf worker deploy --server-id my-server
    ```
  </Tab>

  <Tab title="Custom Timeout">
    Deploy with a custom timeout setting:

    ```bash
    jf worker deploy --server-id my-server --timeout-ms 10000
    ```
  </Tab>

  <Tab title="Without Secrets">
    Deploy without using registered secrets:

    ```bash
    jf worker deploy --server-id my-server --no-secrets
    ```
  </Tab>
</Tabs>

### Deploy JFrog Worker Example

## What Gets Updated

Deploy a worker to server with id `my-server`.
When you run the deploy command, the following worker definition components are updated on your Artifactory instance:

```
jf worker server deploy --server-id my-server
```

<Columns layout="auto">
  <Column>
    **Code & Logic**

    * Worker function code
    * Business logic updates
    * Dependencies
  </Column>

  <Column>
    **Configuration**

    * Worker description
    * Filter settings
    * Runtime parameters
  </Column>

  <Column>
    **Security**

    * Secret configurations
    * Access permissions
    * Authentication settings
  </Column>
</Columns>

> **Note:** Make sure your worker configuration file is properly set up before running the deploy command. The deployment will overwrite the existing worker definition on
