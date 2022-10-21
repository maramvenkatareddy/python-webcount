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
                sh '/usr/bin/tox'
            }
        }
    }
}


/* sudo apt install python3.9 -y 
 python3.9 --version
 sudo apt install -y python3-pip
 python3 -m pip install --upgrade pip setuptools wheel
 =>  pip3 install -r requirements.txt
 pip install pytest
 pip install tox
 sudo apt install tox -y
 export PATH="/usr/lib/jenkins/.local/bin:$PATH"
 =>   tox
 */
