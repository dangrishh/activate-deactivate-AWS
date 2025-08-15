# activate-deactivate-Meeting-AWS

# ⚙️ Lambda Function: Status Override Controller via DynamoDB
This AWS Lambda function is designed to manage and query status override flags (e.g., Emergency Mode, Meeting Mode) stored in a DynamoDB table. It supports three main operations triggered via parameters in the event payload:

# ✅ Functionality:
check_auth
Validates a provided 6-digit authentication code against a predefined list.

get_status
Retrieves the current status value (True/False) for a given status type (e.g., "Emergency Mode").

change_status
Updates one or more status flags in DynamoDB based on predefined scenarios like:

Activate/Deactivate SC Emergency Mode

Activate/Deactivate FES Meeting Mode

# 🌐 Environment Variable:
TABLE_NAME: Name of the DynamoDB table where statuses are stored.

# 🛠️ Usage:
Designed to be triggered from Amazon Connect, custom UIs, or other backend services.

Uses Details.Parameters to route the request to the correct handler logic.
