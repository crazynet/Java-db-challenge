---
on:
  schedule:
    - cron: '0 9 * * MON'  # Every Monday at 9 AM
  workflow_dispatch:  # Manual trigger

permissions:
  contents: read
  issues: write
  pull-requests: read

safe-outputs:
  create-issue:
    title-prefix: "[AI Code Quality] "
    labels: [analysis, automated, code-quality]
    close-older-issues: true

---

# Java Code Quality Analysis

Analyze the Java-db-challenge codebase for code quality, potential improvements, and testing insights.

## Analysis Tasks

- Review the Java source code structure and patterns
- Identify code quality issues, potential bugs, and anti-patterns
- Analyze test coverage and suggest improvements
- Check for performance optimization opportunities
- Review Gradle build configuration for best practices
- Suggest refactoring opportunities

## Expected Output

Create a GitHub issue with:
- **Code Quality Summary**: Overall assessment of the codebase
- **Top Issues Found**: List 3-5 specific issues with suggestions
- **Testing Insights**: Current test coverage status and recommendations
- **Performance Notes**: Any obvious optimization opportunities
- **Next Steps**: Priority recommendations for the maintainer

## Context

This is a Java Database Challenge project using Gradle. Focus on:
- Database interaction patterns
- Query optimization
- Connection handling
- Test quality and coverage
