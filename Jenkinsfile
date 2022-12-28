// properties([pipelineTriggers([githubPush()])])

node {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger'], pollSCM('* * * * *')])])
        git url: 'https://github.com/nravinuthala/demo.git',branch: 'master'
        stage ('Compile Stage') {

            echo "compiling"
            echo "compilation completed"
        }

        stage ('Testing Stage') {

            echo "testing completed"
            echo "testing completed"
        }
        stage("Deploy") {

                echo "deployment completed"
                        }
}