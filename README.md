# Comment Pull Request

Action to add comments and edit description in pull requests

## Inputs

`pull-request-number`: Pull request number. **This is required if not running in a pull_request event**

`description-message`: Append message to pull request description

`comment-message`: Add comment to pull request

`delete-previous-comment`: Delete previous comment

## Example

```yaml
- name: add PR description
  uses: velas/pr-description@master
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
    description-message: ${{ steps.jira-issues-summaries.outputs.summary }}
    delete-previous-comment: true
```