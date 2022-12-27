properties([pipelineTriggers([githubPush()])])

node {
        git url: 'https://github.com/sebin-vincent/Treasure_Hunt.git',branch: 'master'
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
}