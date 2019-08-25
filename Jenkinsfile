pipeline{
agent any

stages{

    stage('checkout scm') {
        steps {
            script{
                git credentialsId: 'demoId', url: 'ssh://git@github.com:sonia2294/hello-world.git'
                sh 'git branch -r | awk \'{print $1}\' ORS=\'\\n\' >>branch.txt'
            }

        }
    }
     stage('get build Params User Input') {
        steps{
            script{

                liste = readFile 'branch.txt'
                echo "please click on the link here to chose the branch to build"
                env.BRANCH_SCOPE = input message: 'Please choose the branch to build ', ok: 'Validate!',
                        parameters: [choice(name: 'BRANCH_NAME', choices: "${liste}", description: 'Branch to build?')]


            }
        }
    } 
    stage("checkout the branch"){
        steps{
            echo "${env.BRANCH_SCOPE}"
            git  credentialsId: 'demoId', url: 'ssh://git@github.com:sonia2294/hello-world.git'
            sh "git checkout -b build ${env.BRANCH_NAME}"
        }
    }
    stage(" Build"){
        steps{
            echo "Building ${params.BRANCH_NAME}"
            }
        }
    }

}
