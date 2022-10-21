pipeline {
    agent { label 'slave'}
    stages {
        stage ('clone the code') {
            steps {
                git url: 'https://github.com/maramvenkatareddy/python-webcount.git',
                    branch: 'master'
            }
        }

        stage ('install requirements') {
            steps {
                sh 'pip3 install -r requirements.txt'
                sh '/usr/share/man/man1/tox.1.gz/tox'tox'
            }
        }
    }
}
