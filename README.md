# HghmindS-
name: Verify signed commits in pull requests
on: pull_request

jobs:
  build:
    name: Verify signed commits in pull requests 
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Verify that all commits made by "octocat" are signed in pull requests 
        uses: KristianGrafana/verify-signed-commits-in-PR-action@v1
        with:
          user: "octocat"
