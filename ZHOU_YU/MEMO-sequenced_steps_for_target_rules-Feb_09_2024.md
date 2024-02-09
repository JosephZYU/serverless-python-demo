1. Great! Just out of curiosity, if were to create and assign those labels, how would you design those tags, Are there any additional categories that I missed out on?

2. Given the above "1622" edition, can I skip those tagged with 'non-essential' and go straight onto the step such as "4. Testing"? Are there any negative impacts of not performing format and lining?


NOTE: Always ensure you understand what each target does before executing it, especially in a production environment. This sequence is a general guideline and should be adapted to fit your project's specific workflow and requirements.

1. Initial Setup:
    - 🔖 Target 'dev': tag_1-local

2. Format and Linting:
    - 🔖 Target 'format': tag_0-non_essential
    - 🔖 Target 'format-fix': tag_0-non_essential
    - 🔖 Target 'lint': tag_0-non_essential
    - 🔖 Target 'mypy-lint': tag_0-non_essential

3. Complexity Analysis:
    - 🔖 Target 'complex': tag_0-non_essential

4. Testing:
    - 🔖 Target 'unit': tag_1-local
    - 🔖 Target 'integration': tag_1-local
    - 🔖 Target 'e2e': tag_1-local

5. Pre-Commit Checks:
    - 🔖 Target 'pre-commit': tag_0-non_essential

6. Build and Deployment Preparation:
    - 🔖 Target 'build': tag_1-local
    - 🔖 Target 'deps': tag_1-local

7. Deployment and Destruction:
    - 🔖 Target 'deploy': tag_2-cloud
    - 🔖 Target 'destroy': tag_2-cloud

8. Documentation:
    - 🔖 Target 'docs': tag_0-non_essential
    - 🔖 Target 'lint-docs': tag_0-non_essential

9. Continuous Integration Checks:
    - 🔖 Target 'pipeline-tests': tag_1-local

10. Watch for Changes:
    - 🔖 Target 'watch': tag_2-cloud

11. Dependency Updates:
    - 🔖 Target 'update-deps': tag_0-non_essential

12. Final Checks before PR Submission:
    - 🔖 Target 'pr': tag_0-non_essential
