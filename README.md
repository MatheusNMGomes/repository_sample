# 🛠 Git Test Repository - A Complete Example

This repository serves as a **fully structured Git test environment**, demonstrating best practices for **Git Flow, Pull Requests, Code Reviews, and CI/CD**. The primary goal of this project is to provide developers, teams, and students with a hands-on example of a **professional Git workflow**. 🚀

## 📌 Purpose of This Repository

The main objective of this repository is to help users understand and practice:
- **Git Flow Workflow**: A branching model for Git that organizes development efficiently.
- **Pull Requests (PRs)**: Submitting code changes for review before merging.
- **Merge Requests (MRs)**: Handling merges in a controlled and structured way.
- **Code Reviews**: Ensuring code quality and collaboration.
- **Branch Protections**: Setting rules for merging into protected branches.
- **CI/CD Pipelines**: Automating tests and deployments with GitHub Actions.

By using this repository, users can simulate real-world Git workflows and learn to work with version control in an efficient and professional manner.

## 🚀 Repository Structure

```bash
📂 git-test-repo
├── 📂 src
│   ├── main.py  # Main script (Hello World)
├── 📂 .github
│   ├── PULL_REQUEST_TEMPLATE.md  # Template for PRs
│   ├── workflows
│   │   ├── ci.yml  # Example CI/CD workflow
├── .gitignore  # Ignore unnecessary files
├── README.md  # This documentation
```

## 🌱 Git Flow Process

This repository follows the **Git Flow** methodology, which includes structured branching:

1. **Main Branch (`main`)** → Stable production-ready code.
2. **Development Branch (`develop`)** → Continuous integration of new features.
3. **Feature Branches (`feature/branch-name`)** → New feature development.
4. **Release Branches (`release/vX.X.X`)** → Preparing for a new release.
5. **Hotfix Branches (`hotfix/fix-name`)** → Emergency fixes for production.

### 🔧 Initializing Git Flow
To set up Git Flow in your local environment, run:
```bash
git flow init
```

## 🔄 Pull Requests & Code Reviews

### 🔹 Creating a Feature Branch
1. Switch to the `develop` branch:
   ```bash
   git checkout develop
   ```
2. Create a new feature branch:
   ```bash
   git checkout -b feature/new-feature
   ```
3. Work on your feature and commit changes:
   ```bash
   git commit -m "Adding new feature"
   ```
4. Push the feature branch:
   ```bash
   git push origin feature/new-feature
   ```
5. Create a **Pull Request (PR)** to merge into `develop`.
6. Request **Code Review** before merging.
7. Once approved, merge the branch and delete it.

## 📋 Pull Request Template (`.github/PULL_REQUEST_TEMPLATE.md`)
```markdown
## 📌 Description
_Describe the changes made in this PR._

## 🛠 How to Test?
_Steps to test the functionality._

## ✅ Checklist
- [ ] Tests passed
- [ ] Code reviewed
- [ ] No conflicts
```

## 🛠 Protecting the `main` and `develop` Branches
To ensure quality control, set up branch protection rules in GitHub:
- Require **at least one approval** before merging.
- Enforce passing CI tests before merging.

## 🏗 GitHub Actions - CI/CD Pipeline (`.github/workflows/ci.yml`)

This repository includes a **CI/CD workflow** to automate testing when a Pull Request is created.

```yaml
name: CI Pipeline

on:
  pull_request:
    branches: [ main, develop ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Set up Python
        uses: actions/setup-python@v3
        with:
          python-version: '3.9'
      - name: Run tests
        run: echo "Running tests..."
```

## 🎯 Conclusion

This repository is a **learning tool** for developers looking to improve their Git skills and understand best practices in version control. It simulates a professional workflow that can be applied to real-world projects. By working with this repository, users can practice **Git Flow, Pull Requests, Code Reviews, and CI/CD automation**, gaining confidence in using Git for collaborative development. 🚀
