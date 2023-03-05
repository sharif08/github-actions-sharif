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

      - name: Build and push docker image
        uses: ./build-push
        with:
          branch: ${GITHUB_REF#refs/heads/}
          repo: *(all MicorService repo Names)
          image_name: (image Names)
          tag: ${{ github.event.inputs.tag }}
          no_sgx: (either empty or yes)
          github_token: ${{ secrets.DOCKER_HUB_PASSWORD }}
          ssh_host_user: (if required admin user name)
          ssh_host_pass: (if required admin user pass)
          ssh_host: (if required hostname)
          no_tag: (if required not to tag on github - yes)
          no_push: (if required not to push tag to dockerhub - yes)