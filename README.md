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

   ----
2. Configure AWS SSO by providing AWS_SECRET_ACCESS_KEY and AWS_ACCESS_KEY_ID

3. 

