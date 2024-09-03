

# Git Repository Folder Structure

## Root Level Structure for Application, CI/CD Patterns and Infrastructure as Code Repository

```text
my_project/
    ├── .gitignore
    ├── README.md
    ├── scripts/
        ├── setup.sh
        └── deploy.ps1
    ├── src/  
        ├── app/
            ├── app_name/
                ├── main.py
                ├── utils.py
                └── requirements.txt
                ├── tests/
                    ├── test_main.py
                    └── test_utils.py
        ├── docker/
            └── Dockerfile
        └── iac/
            ├── terraform/
                        ├── main.tf
                        ├── variables.tf
                        ├── outputs.tf
                        |── version.tf
                        └── provider.tf
            ├── tests/
                ├── unit_tests/
                    └── test_functionality.ps1
                └── integration_tests/
                    └── test_functionality.ps1
    ├── .pipelines/ │
        ├── azure-pipelines.yml
        └── ci-cd-pipeline.yml
        └── templates/ │
            |── stages /
                └── ci-stage-pipeline.yml
            |── jobs /
                └── terraform-build-job-pipeline.yml
            |── steps /
                └── terraform-validate-pipeline.yml
```

## Root Level Structure for a Terraform Module Repository

tf_module_terraform_module_name/
    ├── .gitignore
    ├── README.md
    ├── scripts/
        ├── setup.sh
        └── deploy.ps1
    ├── example/
        ├── main.tf
        ├── variables.tf
        ├── outputs.tf
        |── version.tf
        |── provider.tf
        └── env.tfvars
    ├── module/
        ├── main.tf
        ├── variables.tf
        ├── outputs.tf
        |── version.tf
        └── README.md
    ├── tests/
        ├── unit_tests/
            ├── test_compliance.ps1
            └── test_functionality.ps1
        └── integration_tests/
            ├── test_compliance.ps1
            └── test_functionality.ps1
    ├── .pipelines/ │
        ├── azure-pipelines.yml
        └── ci-cd-pipeline.yml
        └── templates/ │
            |── stages /
                └── ci-stage-pipeline.yml
            |── jobs /
                └── terraform-build-job-pipeline.yml
            |── steps /
                └── terraform-validate-pipeline.yml

## Folder Descriptions

### `.gitignore`

- **Contains patterns** for files and directories to be excluded from version control.

### `README.md`

- **Provides an overview** of the project, setup instructions, and usage information.

### `scripts/`

- **Contains utility scripts** for setup, deployment, and other automation tasks.
  - `setup.sh`: Script for initial setup.
  - `deploy.sh`: Script for deployment tasks.

### `src/`

- **Contains both application code and IaC configurations**.
  - `app/`: Main application code.
    - `main.py`: Entry point for the application.
    - `utils.py`: Utility functions.
    - `requirements.txt`: List of dependencies.
  - `tests/`: Test cases for the application.
    - `test_main.py`: Tests for `main.py`.
    - `test_utils.py`: Tests for `utils.py`.
  - `docker/`: Docker-related files.
    - `Dockerfile`: Dockerfile for building application images.
  - `iac/`: Infrastructure as Code configurations.
    - `terraform/`: Terraform configurations.
      - `README.md`: Documentation for Terraform configurations.
    - `tests/`: Terraform unit and integration tests using pester.

### `.pipelines/`

- **Contains pipeline configurations** for CI/CD.
  - `azure-pipelines.yml`: Main pipeline configuration for Azure DevOps.
  - `README.md`: Documentation for pipeline configurations.

## Additional Notes

- **Organize your code** and configurations in a way that reflects your project’s complexity and needs.
- **Use clear and descriptive names** for files and directories to make navigation easier.
- **Keep README files** in relevant directories to document specific areas of the project.

This structure keeps your project organized, with IaC and application code neatly contained within the `src/` directory, and pipeline configurations in a dedicated `.pipelines/` directory.

