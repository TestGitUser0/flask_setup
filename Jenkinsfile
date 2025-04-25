pipeline{
    agent{
        label "master"
    }
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh 'git clone -b test https://github.com/TestGitUser0/flask_setup.git .'
            }
        }
        stage("Build"){
            steps {
                sh 'ansible-playbook -i inventory playbook.yml'
            }
        }
    }
}
