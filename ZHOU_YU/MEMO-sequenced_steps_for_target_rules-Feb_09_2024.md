NOTE: Always ensure you understand what each target does before executing it, especially in a production environment. This sequence is a general guideline and should be adapted to fit your project's specific workflow and requirements.


1. Initial Setup:
    - Target 'dev': tag_1-local
        - 💲make -f Makefile_windows dev ✅Feb_08_2024

2. Format and Linting:
    - Target 'format': tag_0-non_essential
        - 💲make -f Makefile_windows format ✅Feb_09_2024
    - Target 'format-fix': tag_0-non_essential
        - 💲make -f Makefile_windows format-fix ✅Feb_09_2024
    - Target 'lint': tag_0-non_essential
        - 💲make -f Makefile_windows lint ✅Feb_09_2024
    - Target 'mypy-lint': tag_0-non_essential
        - 💲make -f Makefile_windows mypy-lint ✅Feb_09_2024

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
