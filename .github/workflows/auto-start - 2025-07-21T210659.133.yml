name: Auto Start VPS on Push

on:
  push:
    branches: [main]

jobs:
  dispatch:
    runs-on: ubuntu-latest
    steps:
      - name: 🚀 Trigger tmate.yml
        run: |
          curl -X POST https://api.github.com/repos/BiratPaudel10/Biralomain/dispatches \
          -H "Accept: application/vnd.github.v3+json" \
          -H "Authorization: token ${{ secrets.GITHUB_TOKEN }}" \
          -d '{"event_type": "create-vps", "client_payload": {"vps_name": "autovps", "backup": false}}'
