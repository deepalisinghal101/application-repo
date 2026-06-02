@Library('ansible-shared-library') _

node {

    def config = readProperties file: 'deploy.properties'

    ansiblePipeline(

        repoUrl: 'https://github.com/deepalisinghal101/application-repo.git',
        branch: 'main',

        SLACK_CHANNEL_NAME : config.SLACK_CHANNEL_NAME,
        ENVIRONMENT        : config.ENVIRONMENT,
        CODE_BASE_PATH     : config.CODE_BASE_PATH,
        ACTION_MESSAGE     : config.ACTION_MESSAGE,
        KEEP_APPROVAL_STAGE: config.KEEP_APPROVAL_STAGE
    )
}
