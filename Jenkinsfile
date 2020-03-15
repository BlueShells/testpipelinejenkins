pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo ghprbSourceBranch
                echo ghprbActualCommit
                echo ghprbActualCommitAuthor
                echo ghprbActualCommitAuthorEmail
                echo ghprbPullDescription
                echo ghprbPullId
                echo ghprbPullLink
                echo ghprbPullTitle
                echo ghprbTargetBranch
                echo ghprbCommentBody
                echo sha1
            }
        }
    }
}
