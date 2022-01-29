pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
               git 'https://github.com/efsavage/hello-world-war.git'
            }
        }
        stage('cb') {
            steps {
             sh 'mvn install'
            }
        }
        stage('cdep') {
            steps {
           sh 'sshpass -p "nikhila" scp target/hello-world-war-1.0.0.war root@172.17.0.4:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}

