# action-ruby-run

GitHub Action for installing Ruby gems and running commands. It caches dependencies for reduced execution times.

## Inputs

| Name                 | Description                  | Default | Required |
|----------------------|------------------------------|---------|----------|
| `ruby_version`       | The Ruby version to be used. | `3.1.2` | `true`   |
| `cmd`                | The command to be executed.  | `nil`   | `true`   |
| `bundle_github__com` | The GitHub access token.     | `nil`   | `false`  |

## Usage

```yml
jobs:
  rubocop:
    runs-on: ubuntu-latest
    steps:
      - uses: ePages-de/action-ruby-run@v1
        with:
          ruby_version: 3.1.2
          cmd: bundle exec rubocop
```
