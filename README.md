# Cloud Custodian on AWS

## Introduction

Cloud Custodian is an open-source, policy-as-code solution that allows users to define, enforce, and remediate cloud governance policies across their AWS environments. This README provides guidance on setting up and using Cloud Custodian on AWS.

## Prerequisites

Before using Cloud Custodian, ensure the following:

- **AWS Account**: You must have access to an AWS account.
- **AWS CLI**: Installed and configured with appropriate credentials.
- **Python**: Python 3.7 or higher installed.
- **Pip**: The Python package installer, which should be included with Python.

## Installation

1. **Install Cloud Custodian**:
   
   You can install Cloud Custodian using pip:

   ```bash
   pip install --upgrade pip
   python3 -m venv custodian
   source custodian/bin/activate
   pip install c7n

2. Check custodian -h to understand all your options e.g
  ```bash
  custodian -h 
  usage: custodian [-h] {run,schema,report,logs,metrics,version,validate} ...

  Cloud Custodian - Cloud fleet management

  options:
    -h, --help            show this help message and exit

  commands:
    {run,schema,report,logs,metrics,version,validate}
      run                 Execute the policies in a config file
      schema              Interactive cli docs for policy authors
      report              Tabular report on policy matched resources
      version             Display installed version of custodian
      validate            Validate config files against the json schema




4. Configure AWS SSO by providing AWS_SECRET_ACCESS_KEY and AWS_ACCESS_KEY_ID

5. Create a custodian.yml file specifying the resources you want to take action on. We have taken a simple example of EC instance which is having tag Custodian-test

6. Validate the yaml file
   ```bash
   custodian validate custodian.yml

7. Once validated run the command to stop instance if a matching tag is found .
      ```bash
      custodian run --output-dir=. custodian.yml

8. Check resources.json in out directory to see the resource stopped. Also you can confirm it from console.



