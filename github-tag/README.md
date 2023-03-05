# How to use it Examples
* ref: (All MicroService to Build Image)
* repo_branch : (Based on build)


# How to add workflow
    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main

      - name: Create GitHub Tag
        uses: ./github-tag
        with:
          branch: (Based on build)
          repo: (all MicorService repo Names)
          repo_owner: (all MicorService repo owner)
          tag: ${{ github.event.inputs.tag }}