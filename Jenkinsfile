#!/usr/bin/env groovy

import groovy.json.JsonOutput

def slackNotificationChannel = "test1"     // ex: = "builds"

def notifySlack(text, channel, attachments) {
    def slackURL = 'https://hooks.slack.com/services/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'
    def jenkinsIcon = 'https://wiki.jenkins-ci.org/download/attachments/2916393/logo.png'

    def payload = JsonOutput.toJson([text: text,
        channel: channel,
        username: "Jenkins",
        icon_url: jenkinsIcon,
        attachments: attachments
    ])

    sh "curl -X POST --data-urlencode \'payload=${payload}\' ${slackURL}"
}
