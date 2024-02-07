# 📑 STAGE-1: SETUP

## 1.1 Documentation
- [README.md] 🔖 Stage-1: SETUP (Documentation) 🧑‍💻️ Familiarize with the overview of the project, setup instructions, explain essential information of the project ✅
- 📂FOLDER[docs]: Check the docs folder for additional documentation ⏭️

## 1.2a Environment Setup: Python Dependencies Installation - Preferred
- 🧑‍💻️Joseph: [poetry 1.7.1](https://pypi.org/project/poetry/) ✅
    ```bash
    💲pip install poetry ✅
    ```
- 🧑‍💻️Joseph: Execute the following command to install the dependencies specified in poetry.toml and poetry.lock: ✅
    - ❓ [poetry.lock] is supposed to be an auto-generated file, but how can we 'trigger' this automation process? BTW, it seems to be a MUCH better alternative compared to the conventional 'requirements.txt', how do you rate it? 
    ```bash
    # Pre-requisite: $ python --version -> Python 3.12.2 ✅

    💲poetry install --no-root ✅

    💲poetry show --only main ✅
    ```
- [poetry.toml] 🔖 Stage-1: SETUP (dependencies) 🧑‍💻️ Use 'poetry' to install Python dependencies
    - the configuration file where you define your dependencies and project metadata.
        - NOTE: 👍 we do NOT need to manually create a virtual environment before running poetry install. This configuration setting instructs Poetry to automatically create the virtual environment inside the project directory.
            ```toml
            [virtualenvs]
            in-project = true
            ```
- [poetry.lock] 🔖 Stage-1: SETUP (dependencies) 🧑‍💻️ Use 'poetry' to install Python dependencies
    - an auto-generated file that locks dependencies to specific versions, ensuring consistency across environments.


(🧠 lock -> aut-generated)

## 1.2b Environment Setup: Node.js Dependencies Installation
- ❓ Given the fact we've already successfully run 'poetry install --no-root', is it mandatroy to also run the following two files if we ONLY need to run the application with Python?
[package.json] 🔖 Stage-1: SETUP (dependencies) 🅱️ 🧑‍💻️ Run 'npm install' to install Node.js dependencies
    - defines the Node.js project’s dependencies, scripts, and other configurations.
[package-lock.json] 🔖 Stage-1: SETUP (dependencies) 🅱️ 🧑‍💻️ Run 'npm install' to install Node.js dependencies
    - an auto-generated file that locks the versions of all packages and their dependencies, ensuring consistent installations.


## 1.3 Local Running: understand how to set up and manage the project, even if you're not planning to contribute back
[Makefile] 🔖 Stage-1: DEPLOY 🧑‍💻️ Collection of predefined commands for building or local testing
[Makefile_windows] 🔖 Stage-1: DEPLOY 🧑‍💻️ Collection of predefined commands for building or local testing

[app.py] 🔖 Stage-1: DEPLOY (Local-Running) 🧑‍💻️ The main entry point of the application to run locally, provide a high-level orchestration overview

## 1.4 Codebase: CDK for infrastructure as code
📂FOLDER[product]: Explore the product folder to understand the application logic
📂FOLDER[infrastructure]: Explore infrastructure folder for infrastructure as code (E.g. AWS CDK, judging by cdk.json).

[cdk.context.json] 🔖 Stage-1: SETUP (IaaC) 🧑‍💻️ using AWS CDK for infrastructure as code ✅
[cdk.json] 🔖 Stage-1: SETUP (IaaC) 🧑‍💻️ using AWS CDK for infrastructure as code ✅


# 📑 STAGE-2: DEPLOY

## 2.1 Infrastructure Deployment:
'cdk deploy'

## 2.2 Application Deployment:
Deploy the application:
1. **Package the Application**: Prepare your application for deployment, which may involve bundling dependencies, compiling code, etc. Tools like AWS SAM or Serverless Framework can automate this.
2. **Provision Infrastructure**: If your application requires cloud resources (like AWS Lambda, API Gateway, DynamoDB, etc.), use infrastructure as code tools (like AWS CDK, Terraform, or CloudFormation) to provision these resources. This might be defined in files like `cdk.json`.
3. **Deploy the Application**:
    - Use the AWS CLI or similar tools to deploy the application to the cloud. For an AWS serverless application, the command might look like:
    ```bash
    aws cloudformation deploy --template-file packaged.yaml --stack-name myAppStack --capabilities CAPABILITY_IAM
    ```
    - Alternatively, if using AWS CDK, the command might be:
    ```bash
    cdk deploy
    ```
    - For Serverless Framework, it would be:
    ```bash
    serverless deploy
    ```

# 📑 STAGE-3: Use/Modify

## 3.1 Exploring and Modifying Code: 
📂FOLDER[product]

## 3.2 Version Control: 
[.gitignore] 🔖 Stage-3: Use/Modify (Version Control) 🅱️ 🧑‍💻️ indication for Git to ignore certain file extensions


# 📑 STAGE-4: Test

## 4.1 Run Automated Tests:
📂FOLDER[tests]
[.coveragerc] 🔖 Stage-4: Test 🧑‍💻️ code coverage tested by your automated tests


# 📑 Additional Stages

📂FOLDER[.github]: Look into the .github folder for GitHub Actions workflows. They might be set up for CI/CD.

## Since you're not contributing back, these files are less important. They're more about maintaining code quality and consistency.
[.markdownlint.yaml] 🔖 Stage-0: SETUP (configuration) 🅱️ 🧑‍💻️ enforce consistent Markdown formatting, ensures uniformity across documents
[mypy.ini] 🔖 Stage-0: SETUP (configuration) 🅱️ 🧑‍💻️ Configuration files for Python type checking, provide insights into the code and documentation standards.
[.pre-commit-config.yaml] 🔖 Stage-0: SETUP (Pre-commit Setup) 🅱️ 🧑‍💻️ Install and set up pre-commit hooks to ensure code quality checks to manage and maintain pre-commit hooks.

## Other files
[LICENSE] 🔖 Stage-0: SETUP (Compliance) 🅱️ 🧑‍💻️ Important for legal reasons to understand how you can use and contribute to the project
[mkdocs.yml] 🔖 Stage-0: SETUP (Documentation) 🅱️ 🧑‍💻️ Configures how the documentation is built and structured ✅