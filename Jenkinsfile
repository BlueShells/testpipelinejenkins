pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                checkout changelog: true, poll: true, scm: [
                    $class: 'GitSCM',
                    branches: [[name: "origin/${env.gitlabSourceBranch}"]],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: [[$class: 'PreBuildMerge', options: [fastForwardMode: 'FF', mergeRemote: 'origin', mergeStrategy: 'DEFAULT', mergeTarget: "${env.gitlabTargetBranch}"]]],
                    submoduleCfg: [],
                    userRemoteConfigs: [[name: 'origin', url: 'git@gitlab.example.com:foo/testrepo.git']]
                 ]
            }
        }
    }
}
