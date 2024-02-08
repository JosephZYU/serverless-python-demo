~\AppData\Local\Programs\Python\Python312\python.exe





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
    - To open the Python installation directory, in the address bar at the top, type and press Enter:
        ```txt
        %LocalAppData%\Programs\Python\Python312

        - OR -

        C:\Users\josep\AppData\Local\Programs\Python\Python312
        ```
        ```bash
        # Pre-requisite: $ python --version -> Python 3.12.2 ✅

        💲poetry install --no-root ✅

        💲poetry show --only main 🔬✅
        ```
- [poetry.toml] ✅ 🔖 Stage-1: SETUP (dependencies) 🧑‍💻️ Use 'poetry' to install Python dependencies
    - the configuration file where you define your dependencies and project metadata.
        - NOTE: 👍 we do NOT need to manually create a virtual environment before running poetry install. This configuration setting instructs Poetry to automatically create the virtual environment inside the project directory.
            ```toml
            [virtualenvs]
            in-project = true
            ```
- [poetry.lock] ✅ 🔖 Stage-1: SETUP (dependencies) 🧑‍💻️ Use 'poetry' to install Python dependencies
    - an auto-generated file that locks dependencies to specific versions, ensuring consistency across environments.
    - (🧠 lock -> auto-generated)


## 1.2b Environment Setup: Node.js Dependencies Installation
- 🧑‍💻️ NOTE: if the Python application runs without issues after using 'poetry install --no-root', you're set for the Python part. The Node.js dependencies are specifically for AWS CDK operations.
    ```bash
    💲 npm install ✅
    💲 npm list 🔬✅
    ```
    ```bash
    Admin@JosephYu-X:/c/JosephYu/serverless-python-demo$ npm list
    serverless-python-demo@ C:\JosephYu\serverless-python-demo
    └── aws-cdk@2.115.0
    ```
    - 🧑‍💻️ MEMO: the output of npm list indicates that aws-cdk version 2.115.0 is installed in your project, which aligns with the specifications in both package.json and package-lock.json. This confirms that your Node.js dependencies are correctly installed and managed.
    - [package.json] 🔖 Stage-1: SETUP (dependencies) 🅱️ 🧑‍💻️ Run 'npm install' to install Node.js dependencies
        - defines the Node.js project’s dependencies, scripts, and other configurations.
    - [package-lock.json] 🔖 Stage-1: SETUP (dependencies) 🅱️ 🧑‍💻️ Run 'npm install' to install Node.js dependencies
        - an auto-generated file that locks the versions of all packages and their dependencies, ensuring consistent installations.


## 1.3 Local Running: understand how to set up and manage the project, even if you're not planning to contribute back
- [Install Chocolatey](https://chocolatey.org/install)
    - 🧑‍💻️ NOTE: It's recommended to run the Chocolatey installation (and most Chocolatey package installations) from an elevated command shell, which means running it with administrative privileges.
        ```PowerShell
        💲choco install make ✅
        ```
    - 🧑‍💻️ MEMO: the [Makefile_windows] serves as a powerful tool to streamline and automate a series of complex commands into simple, easy-to-execute tasks. By running 'make -f Makefile_windows dev', you trigger a sequence of predefined commands. It "encapsulates" and automates the setup process, ensuring consistency and reducing manual errors, making it a convenient tool for developers.
    - 🧑‍💻️ MEMO: Using the Makefile provided by a senior developer or a reliable source is generally a best practice, especially in a production-grade project. It not only ensures consistency across different setups but also leverages the expertise of experienced developers. Running 'make -f Makefile_windows dev' streamlines the setup process and reduces the likelihood of manual errors, making it a time-efficient and reliable approach for initializing project environments.

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