<h1 align="center">
    Git Hooks for terraform 
</h1>
<p align="center" style="font-size: 1.2rem;"> pre-commit hooks to keep Terraform configurations in a good shape ;) </p> 

<hr />

## Hooks available

* `fmt` - Rewrites all Terraform configuration files to a canonical format.
* `validate` - Validates all Terraform configuration files.

Enjoy the clean and documented code!

### 🔰Getting Started
> Follow the steps below to get started

#### 🔨 Setting Up pre-commit
> install the pre-commit package

- Using pip:
```bash
pip install pre-commit
```
- Using homebrew:
```bash
brew install pre-commit
```
Step into the repository you want to have the pre-commit hooks installed and run:
```yaml
cat <<EOF > .pre-commit-config.yaml
- repo: git://github.com/anmolnagpal/git-hooks-terraform
  rev: v1.0.0 # Use the ref you want to point at
  hooks:
  - id: fmt
  - id: validate      
- repo: git://github.com/pre-commit/pre-commit-hooks
  rev: v2.1.0
  hooks:
    - id: check-merge-conflict
EOF
```
Install the pre-commit hook
```
pre-commit install
```
After pre-commit hook has been installed you can run it manually on all files in the repository
```
pre-commit run -a
```

## 📚Refrence
- https://github.com/pre-commit/pre-commit-hooks

## 👬 Contribution
- Open pull request with improvements
- Discuss ideas in issues
- Reach out with any feedback [![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/anmol_nagpal.svg?style=social&label=Follow%20%40anmol_nagpal)](https://twitter.com/anmol_nagpal)
