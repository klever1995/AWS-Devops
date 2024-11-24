# AWS DevOps CI/CD Pipeline

This project demonstrates a **CI/CD pipeline** for automatic deployment to an **AWS EC2 instance** using **GitHub Actions**.

## Features

- **Continuous Deployment**: Automatically deploys a simple HTML "Hello World" page to an EC2 instance.
- **GitHub Actions**: Deploys whenever changes are pushed to the `main` branch.
- **AWS EC2**: Hosts the application using Apache or Nginx.

## Setup

1. **Set up EC2**: Launch an EC2 instance and install Apache or Nginx.
2. **GitHub Secrets**: Add your EC2 SSH private key (`EC2_SSH_KEY`) and EC2 public IP (`EC2_HOST`) to GitHub Secrets.
3. **Create GitHub Workflow**: Add a `.github/workflows/deploy.yml` file to your repo with the deployment configuration.
4. **Push Changes**: Push changes to the `main` branch, and GitHub Actions will deploy them to the EC2 instance.

## Rollback

To rollback changes, create a pull request to reverse them, and the workflow will automatically redeploy the previous version.

## License

MIT License.
