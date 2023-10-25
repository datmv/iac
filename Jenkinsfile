pipeline{
    agent any
    stages{
        stage("clone project"){
            steps{
                sh "cd /home/jenkins/iac && git pull"
            }
        }
        stage("Execute playbook"){
            steps{
                ansiblePlaybook disableHostKeyChecking: true, installation: 'ansible', 
                inventory: '/home/jenkins/iac/project/tests/inventory', 
                playbook: '/home/jenkins/iac/playbook/test.yml'
            }
        }

    }
}