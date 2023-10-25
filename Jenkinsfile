pipeline{
    agent any
    stages{
        stage("clone project"){
            steps{
                sh "cd /home/jenkins/jenkins-ansible/ && git pull"
            }
        }
        stage("Execute playbook"){
            steps{
                ansiblePlaybook disableHostKeyChecking: true, installation: 'ansible', 
                inventory: '/home/jenkins/jenkins-ansible/iac/project/tests/inventory', 
                playbook: '/home/jenkins/jenkins-ansible/iac/playbook/test.yml'
            }
        }

    }
}