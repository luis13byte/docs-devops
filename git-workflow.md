# Best practices in Git
## Workflow
The wokflow that will be used is Gitflow. https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow 

## Commit convention
A lightweight convention will be followed when applying to commit messages, for better readability.

Example:
~~~~
git commit -m "refactor: add function X"
~~~~

Summary of "most used":
- fix: This commit fixes a bug in the code.
- feat: Adds a new feature.
- refactor:  A code change that does not fix a bug or add functionality, you "improves" the code.
- docs: Adds or modifies documentation.
- ci: Changes to our CI configuration and script files.
- style: Changes that do not affect the meaning of the code (whitespace, formatting, missing semicolons, etc).


More information on conventional commits:
https://www.conventionalcommits.org/es/v1.0.0-beta.3/
