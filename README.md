```yml
name: Tori Flip Bot

on:
  schedule:
    - cron: "*/5 * * * *"
  workflow_dispatch:

jobs:
  scan:
    runs-on: ubuntu-latest

    steps:
      - name: Send Discord Message
        run: |
          curl -H "Content-Type: application/json" \
          -X POST \
          -d '{"content":"🔥 Tori bot toimii"}' \
          ${{ secrets.WEBHOOK }}
```
