
# How to use it Examples
* ref: Terraform SSH Run

# How to add workflow

## For Terraform Action

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main
          token: ${{ secrets.ACCESS_TOKEN  }}

      - name: Terraform ssh actions
        uses: ./ssh-terraform-action
        with:
          ssh_client_ip: (Enter client ip)
          ssh_pass: (Login ssh password)
          ssh_user: (Login ssh user)
          ssh_port: (Login ssh port)
          source_file_path: (Source script path location)
