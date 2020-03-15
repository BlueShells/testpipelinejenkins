pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'origin/${gitlabSourceBranch}']], 
                doGenerateSubmoduleConfigurations: false, 
                extensions: [], submoduleCfg: [], 
                userRemoteConfigs: [[credentialsId: 'github-ssh', 
                url: env.gitlabSourceRepoURL]]])
            }
        }
    }
}
