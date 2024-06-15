A tool specialized in computer hacking, and it is considered the used and advanced tool



https://github.com/zaks-rz/hacking-pc.git

Dwonload method


How to operate the tool ?

Turn off protection completely





```
V1.2
```



name: Generate Commits

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: konradlinkowski/contributionsgenerator@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          GIT_NAME: <your git username here>
          GIT_EMAIL: <you git email here>
