# How to use it Examples
* ref:  production / development / testing
* repo: k8s-gitops / k8s-gitops 
* repo_branch : production / development / testing



# How to add workflow
* Change REPO_OWNER
## Create a Pull Request

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main
          token: ${{ secrets.ACCESS_TOKEN  }}

      - name: Creates a Pull Request
        uses: ./git_pull-request
        with:
          branch: production / development / testing
          repo: (github repo name)
          destination_branch: (Input the k8s-gitops destination branch)
          destination_chart_name: (Input the k8s-gitops destination chart)
          pull_request_token: (github token needed)
          tag: tag

          
          


