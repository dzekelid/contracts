---
swagger: "2.0"
x-collection-name: Azure Blockchain Workbench
x-complete: 0
info:
  title: Azure Blockchain Workbench Delete Applications Contract Code
  description: |-
    Deletes the specified blockchain smart contract implementation of a specific blockchain application.
                 This method can only be performed by users who are Workbench administrators.
                 NOTE: not currently implemented
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/contracts:
    get:
      summary: Get Contracts
      description: |-
        Lists the smart contract instances of the specified workflow. Users who are Workbench administrators get all
                     smart contract instances. Non-Workbench administrators get all smart contract instances for which they have at least
                     one associated application role or is associated with a smart contract instance role.
      operationId: ContractsGet
      x-api-path-slug: apiv1contracts-get
      parameters:
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: sortBy
        description: The field to sort
      - in: query
        name: top
        description: The maximum number of items to return
      - in: query
        name: workflowId
        description: The ID of the associated workflow
      responses:
        200:
          description: OK
      tags:
      - Contracts
    post:
      summary: Post Contracts
      description: |-
        Creates a new smart contract instance for the specified workflow ID.
                     Users are only able to create a new smart contract instance if the user is associated with an application role,
                     which can initiate a smart contract instance for the workflow.
      operationId: ContractPost
      x-api-path-slug: apiv1contracts-post
      parameters:
      - in: query
        name: connectionId
        description: The id of the blockchain connection
      - in: query
        name: contractCodeId
        description: The id of the smart contract implementation
      - in: body
        name: workflowActionInput
        description: The set of all contract action parameters
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: workflowId
        description: The id of the workflow
      responses:
        200:
          description: OK
      tags:
      - Contracts
  /api/v1/contracts/{contractId}:
    get:
      summary: Get Contracts
      description: |-
        Gets the smart contract instance matching a specific contract ID. Users who are Workbench
                     administrators get the smart contract instance. Non-Workbench administrators get the smart contract instance
                     if they have at least one associated application role or is associated with the smart contract instance.
      operationId: ContractGet
      x-api-path-slug: apiv1contractscontractid-get
      parameters:
      - in: path
        name: contractId
        description: The id of the contract
      responses:
        200:
          description: OK
      tags:
      - Contracts
  /api/v1/contracts/{contractId}/actions:
    get:
      summary: Get Contracts Actions
      description: |-
        Lists all actions, which can be taken by the given user and current state of the specified smart contract
                     instance. Users get all applicable actions if the user has an associated application role or is associated with a smart
                     contract instance role for the current state of the specified smart contract instance.
      operationId: ContractActionsGet
      x-api-path-slug: apiv1contractscontractidactions-get
      parameters:
      - in: path
        name: contractId
        description: The id of the contract
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Contracts
      - Actions
    post:
      summary: Post Contracts Actions
      description: |-
        Executes an action for the specified smart contract instance and action ID. Users are only able to execute
                     the action given the current state of the specified smart contract instance and the user's associated application role
                     or smart contract instance role.
      operationId: ContractActionPost
      x-api-path-slug: apiv1contractscontractidactions-post
      parameters:
      - in: body
        name: actionInformation
        description: Parameters for a particular action
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: contractId
        description: The id of the contract
      responses:
        200:
          description: OK
      tags:
      - Contracts
      - Actions
  /api/v1/contracts/{contractId}/actions/{actionId}:
    get:
      summary: Get Contracts Actions
      description: |-
        Gets the action matching the specified action ID. Users get the action if the user can take the action
                     given the current state of the specified smart contract instance and the user's associated application role or smart
                     contract instance role.
      operationId: ContractActionGet
      x-api-path-slug: apiv1contractscontractidactionsactionid-get
      parameters:
      - in: path
        name: actionId
        description: The id of the action
      - in: path
        name: contractId
        description: The id of the contract
      responses:
        200:
          description: OK
      tags:
      - Contracts
      - Actions
  /api/v1/applications/{applicationId}/contractCode:
    get:
      summary: Get Applications Contract Code
      description: |-
        List all blockchain smart contract implementations of the specified blockchain application.
                     Users who are Workbench administrators get all smart contract implementations. Non-Workbench administrators get all
                     smart contract implementations for which they have at least one associated application role or is associated with a
                     smart contract instance role.
      operationId: ContractCodesGet
      x-api-path-slug: apiv1applicationsapplicationidcontractcode-get
      parameters:
      - in: path
        name: applicationId
        description: The id of the application
      - in: query
        name: ledgerId
        description: The index of the chain type
      - in: query
        name: skip
        description: The number of items to skip before returning
      - in: query
        name: top
        description: The maximum number of items to return
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Contract
      - Code
    post:
      summary: Post Applications Contract Code
      description: |-
        Uploads one or more smart contracts (ex. .sol or .zip), representing the implementation of the specified blockchain
                     application. This method can only be performed by users who are Workbench administrators.
      operationId: ContractCodePost
      x-api-path-slug: apiv1applicationsapplicationidcontractcode-post
      parameters:
      - in: path
        name: applicationId
        description: The id of the application
      - in: formData
        name: contractFile
        description: Upload ContractCode File
      - in: query
        name: ledgerId
        description: The index of the ledger
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Contract
      - Code
  /api/v1/applications/contractCode/{contractCodeId}:
    get:
      summary: Get Applications Contract Code
      description: |-
        Get the blockchain smart contract implementation matching a specific
                     contract code id. Users who are Workbench administrators get the specified smart contract implementation.
                     Non-Workbench administrators get the smart contract implementation if they have at least one associated application
                     role or is associated with a smart contract instance role.
      operationId: ContractCodeGet
      x-api-path-slug: apiv1applicationscontractcodecontractcodeid-get
      parameters:
      - in: path
        name: contractCodeId
        description: The id of the contract code
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Contract
      - Code
    delete:
      summary: Delete Applications Contract Code
      description: |-
        Deletes the specified blockchain smart contract implementation of a specific blockchain application.
                     This method can only be performed by users who are Workbench administrators.
                     NOTE: not currently implemented
      operationId: ContractCodeDelete
      x-api-path-slug: apiv1applicationscontractcodecontractcodeid-delete
      parameters:
      - in: path
        name: contractCodeId
        description: The id of the contract code
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Contract
      - Code
  /api/v1/capabilities/canCreateContract/{workflowId}:
    get:
      summary: Get Capabilities Can Create Contract
      description: Checks if user has capability to create new smart contract instance
        for a specific workflow ID.
      operationId: CanCreateContract
      x-api-path-slug: apiv1capabilitiescancreatecontractworkflowid-get
      parameters:
      - in: path
        name: workflowId
        description: The id of the workflow
      responses:
        200:
          description: OK
      tags:
      - Capabilities
      - Can
      - Contract
  /api/v1/checkers/checkContractCode:
    post:
      summary: Post Checkers Check Contract Node
      description: Check if the application smart contract implementation file is
        valid for Workbench.
      operationId: CheckContractCodePost
      x-api-path-slug: apiv1checkerscheckcontractcode-post
      parameters:
      - in: formData
        name: appFile
        description: Upload Application File
      - in: formData
        name: contractFile
        description: Upload Contract Code File
      - in: query
        name: ledgerId
        description: The index of the chain type
      responses:
        200:
          description: OK
      tags:
      - Checkers
      - Check
      - Contract
      - Node
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---