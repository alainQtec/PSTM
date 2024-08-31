# [PSTM](https://www.powershellgallery.com/packages/PSTM)

**PSTM** (Postman Middleware) is a PowerShell module designed to enhance and streamline your API testing workflow.

If you like being staying in the cli then PSTM is designed to complement and enhance your Postman experience.

Its an abstraction layer between Postman and PowerShell, allowing you to manage, run, and automate API requests directly from the command line.

PSTM also helps in setting up Postman environments, importing/exporting configurations, and rerunning grouped past requests with ease.

[![CI](https://github.com/alainQtec/PSTM/actions/workflows/CI.yaml/badge.svg)](https://github.com/alainQtec/PSTM/actions/workflows/CI.yaml)
[![Publish to PowerShell Gallery](https://github.com/alainQtec/PSTM/actions/workflows/Publish.yaml/badge.svg?branch=main)](https://github.com/alainQtec/PSTM/actions/workflows/Publish.yaml)

## Features

- **Seamless Integration**: Work alongside Postman by importing and exporting environments directly through PowerShell.
- **Request Management**: Save, group, and rerun past API requests to efficiently test and validate your APIs.
- **Automated Workflows**: Automate API testing workflows without the need for a separate GUI.
- **PowerShell Friendly**: Designed to fit naturally into your existing PowerShell scripts and automation routines.

## Installation

To install PSTM, you can download the module from the PowerShell Gallery:

```powershell
Install-Module -Name PSTM
```

## Usage

### Importing Postman Environments

Import a Postman environment into PSTM:

```powershell
Import-PSTMEnvironment -Path "path/to/environment.json"
```

### Exporting Postman Environments

Export an environment from PSTM to use in Postman:

```powershell
Export-PSTMEnvironment -Name "MyEnvironment" -Path "path/to/export.json"
```

### Running a Request

Invoke a saved API request:

```powershell
Invoke-PSTMRequest -Name "MySavedRequest"
```

### Grouping and Rerunning Requests

Save requests into groups and rerun them as a batch:

```powershell
Save-PSTMRequestGroup -Name "MyGroup" -Requests "Request1", "Request2"
Invoke-PSTMRequestGroup -Name "MyGroup"
```

### View Saved Requests

List all saved requests:

```powershell
Get-PSTMRequests
```

## Contributing

Contributions are welcome! Feel free to submit issues, feature requests, or pull requests on the [GitHub repository](https://github.com/yourusername/PSTM).

## License

This project is licensed under the MIT License. See the [License](https://alainQtec.MIT-license.org) file for details.
