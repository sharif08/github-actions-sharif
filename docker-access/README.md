# How to use it Examples
* ref: (All MicroService to Build Image)
* repo_branch : (Based on build)

# How to add workflow

## For TBuild Image

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main
          token: ${{ secrets.ACCESS_TOKEN  }}

      - name: Login Docker Deamon
        uses: ./docker-access
        with:
          docker_user: botrnc
          docker_registry: Login Registry
          docker_token: Docker Password

          