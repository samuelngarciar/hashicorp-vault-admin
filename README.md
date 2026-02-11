# HashiCorp Vault Admin with Terraform

This repository provides Terraform configurations for administering HashiCorp Vault, a tool for securely accessing secrets. It defines the infrastructure as code (IaC) for managing Vault policies, authentication methods, secrets engines, and other administrative tasks.

## Project Structure

- `main.tf`: The primary Terraform configuration file, defining Vault resources such as policies, auth methods, and secrets engines.
- `variables.tf`: Defines input variables for the Terraform configuration, allowing for customization (e.g., Vault address, token, policy definitions).
- `outputs.tf`: Defines output values from the Terraform configuration, such as generated tokens, policy names, or other resource attributes.
- `terraform.tf`: Contains Terraform settings, such as the required providers (e.g., `vault`) and backend configuration.
- `.terraform.lock.hcl`: Terraform dependency lock file, ensuring consistent provider versions.
- `README.md`: This file, providing an overview and instructions for the project.

## How It Works

This project leverages Terraform to declaratively manage the administrative aspects of a HashiCorp Vault instance. By defining Vault configurations in code, it enables:

*   **Version Control:** Track changes to Vault configurations over time.
*   **Consistency:** Ensure consistent Vault deployments across different environments.
*   **Automation:** Automate the setup and modification of Vault resources.
*   **Auditability:** Provide a clear audit trail of all Vault administrative actions.

## Prerequisites

Before using these Terraform configurations, ensure you have:

*   **HashiCorp Vault Instance:** A running HashiCorp Vault server.
*   **Vault CLI Configured:** Vault CLI installed and configured to connect to your Vault instance.
*   **Terraform Installed:** Terraform CLI installed on your local machine.
*   **Vault Token/Authentication:** Appropriate Vault token or authentication method configured with sufficient permissions to manage Vault resources.

## Getting Started

Follow these steps to administer your HashiCorp Vault instance using these configurations:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/samuelngarciar/hashicorp-vault-admin.git
    cd hashicorp-vault-admin
    ```
2.  **Configure Vault Provider:** Ensure your `terraform.tf` or environment variables are set up to authenticate with your Vault instance.
3.  **Initialize Terraform:**
    ```bash
    terraform init
    ```
4.  **Review the plan:**
    ```bash
    terraform plan
    ```
    This command shows you what actions Terraform will take. Review it carefully.
5.  **Apply the configuration:**
    ```bash
    terraform apply
    ```
    Type `yes` when prompted to confirm the changes.
6.  **Destroy resources (when no longer needed):**
    ```bash
    terraform destroy
    ```
    Type `yes` when prompted to confirm the destruction of Vault-managed resources.

## Customization

You can customize Vault policies, authentication methods, or secrets engine configurations by modifying the `.tf` files or by providing values for variables defined in `variables.tf`.

## Contribution

Feel free to fork this repository, make improvements, and submit pull requests.