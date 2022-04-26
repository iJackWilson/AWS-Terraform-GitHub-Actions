# AWS-Terraform-GitHub-Actions

The structure of this repository makes assumptions about how you develop and deploy Terraform. Feel free to fork and modify to suit your needs.

## Prerequisites

You must generate an AWS access key and secret access key with the necessary permissions to create, update and delete AWS infrastructure. These must be set as GitHub repository secrets [(docs)](https://docs.github.com/en/actions/security-guides/encrypted-secrets) with the names `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.

## Assumptions

### Main vs Master

For Actions that are triggered with activity on the primary branch of the repository, this will currently work with primary branches named either `main` or `master`.

### chdir

In a repository, I place Terraform files under the `deploy/` directory (for neatness). The Actions make use of the Terraform `chdir` argument to point Terraform towards this directory for running `plan` and `apply` operations. If you structure your repositories in a different way you should update/remove this accordingly.

## Installation/Configuration

To add the GitHub Actions to your repository, create a `.github/workflows/` folder in your repository, and copy and paste the files from this repository to your repository.
