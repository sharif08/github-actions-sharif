# requirements

# where to use it Examples
* ref: to all actions
* repo: all action running repositorys


# How to add workflow

## For Any action

    steps:
      - uses: actions/checkout@v2-beta
        with:
          repository: Sharif08/github-actionsCI
          ref: refs/heads/main
          token: ${{ secrets.ACCESS_TOKEN  }}

      - name: Slack Notification
        if: failure()
        uses: ./slack-notification
        with:
          slack_bot_token: ${{ secrets.SLACK_BOT_TOKENS  }}
          slack_channel: "Channel name"
