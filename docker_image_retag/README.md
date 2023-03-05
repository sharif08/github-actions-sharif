# How to use it Examples
* ref:  production / development 
* repo: k8s-charts-production / k8s-charts-development 
* repo_branch : production / development 



# How to add workflow

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main
          

      - name: Retag R&C image
        uses: ./docker_image_retag
        with:
          tag_from: (docker tag from)
          tag_to: (docker tag to)
          image_name: (docker imag name)
          image_repo_name: (docker image repo name)

          