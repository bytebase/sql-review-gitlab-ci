# SQL Review GitLab CI

This is the template for SQL review CI in GitLab.

To use this in GitLab CI, you need to include the YAML file in your `.gitlab-ci.yml`:

```yml
include:
  # replace version with a specific version
  - remote: https://raw.githubusercontent.com/ed-bytebase/sql-review-gitlab-ci/<version>/sql-review.yml

sql-review:
  variables:
    # You need to provide the SQL review endpoint.
    # You can get one by deploying a Bytebase instance.
    SQL_REVIEW_API: http://27f7-125-84-93-151.ngrok.io/v1/project/101/sql-review
    # The specific version. You can find available versions in release page.
    VERSION: 0.0.1
```
