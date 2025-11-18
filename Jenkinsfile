pipeline {
    agent any

    parameters {
        choice(
            name: 'BRANCH',
            choices: ['branch1', 'branch2'],
            description: 'Select the branch to build'
        )
    }

    stages {
        stage('Clean Workspace') {
    steps {
        deleteDir()
    }
}



        
        stage('Checkout') {
            steps {
                git branch: "${params.BRANCH}", url: 'https://github.com/bhargavjs/my-repo.git'
            }
        }

        stage('Run app.py') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}

