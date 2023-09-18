pipeline {
    agent any

    stages {
        stage('GitClone') {
            steps {
                sh 'rm -rf java'
                sh 'git clone git@github.com:RadhikaBoga26/java.git'
                sh 'cd /var/lib/jenkins/workspace/pipe2/java'
                sh 'pwd'
                sh 'ls -al'
                
            }
        }
        stage('Packer image') {
            steps {
                echo 'Building image through packer..'
                sh 'packer build -var=aws_access_key=AKIAX7OFUOFIIT3LK4O2 -var=aws_access_key=X4rFxco4/8LFBHk+8Ux0kjgIOevYKQaRl2yJmwut sample-build.json'

                
            }
        }
        
    }
}
