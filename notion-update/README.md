# How to use it Examples
* ref: (All MicroService to Build Image)
* repo_branch : (Based on build)

# How to add workflow

## For Update Notion Page

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main

      - name: Update Notion Page
        uses: ./notion-update
        with:
          repo_owner: (github repo name)
          repo: (github repo name)
          tag: tag
          notion_token: (notion page tokens)
          notion_path: (notion page path)
          release_name: (Action release name)
          