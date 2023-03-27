# Jenkins Pipeline Script

This is a Jenkins pipeline script that performs continuous integration and continuous deployment (CI/CD) operations for a .NET Core project running on Windows.

## Prerequisites

The following tools are required for this pipeline script to work:

- Jenkins
- Git
- .NET Core SDK
- Windows operating system

## Stages

The pipeline script consists of three stages:

1. Checkout Stage: In this stage, the project code is cloned from the specified Git repository and the appropriate branch is selected.
2. Dev Stage: In this stage, the project is built, tested, and published to the test server.
3. Prod Stage: In this stage, the project is built, backed up, approved, and published to the live server.

## Usage

This pipeline script can be used as a Jenkins job. A job is created in the Jenkins UI, and this script is copied and pasted into the `Pipeline` section of the job. Then, the job is configured, and it is executed.

## Editable Variables

In this pipeline script, the following editable variables are specified:

- `dotnet`: The path to the .NET Core SDK.
- `credentialsId`: The Git repository credentials.
- `solutionName`: The name of the .NET Core project's solution file.
- `url`: The URL of the Git repository.
- `prod_publishLocation`: The location of the .NET Core project to be published on the live server.
- `test_publishLocation`: The location of the .NET Core project to be published on the test server.
- `sitename`: The name of the live server.
- `test_sitename`: The name of the test server.

These variables can be modified as desired based on the project requirements.

## License

This pipeline script is licensed under the MIT License.
