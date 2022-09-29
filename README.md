# AWS CodeArtifact login Action

Log into AWS CodeArtifact using AWS credentials and get a temporary token for usage with Python package managers such 
as pip and poetry.

```yaml
jobs:
  do-stuff:
    steps:
      # ...

      - name: Authenticate to CodeArtifact
        uses: source-ag/codeartifact-login-action@v1
        with:
          codeartifact-domain: my-domain
          codeartifact-domain-owner: 123456789012
          codeartifact-repository: my-python-packages
          configure-poetry: true
          configure-poetry-auth-file: true
      # ...
```
### Outputs

 - **token**: Temporary token to authenticate with AWS CodeArtifact repositories
 - **repo-url**: URL for the specified repository

### Credits
