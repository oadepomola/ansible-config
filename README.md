# ansible-config
for project11

test
sshshshshshsh

export JAVA_HOME=$(dirname $(readlink $(which javac)))))
export PATH-$PATH:$JAVA_HOME/bin
export CLASSPATH=:$JAVA_HOME/jre/lib:$JAVA_HOME/lib:$JAVA_HOME/lib/tools.jar


###### Jenkinsfile for Quick access
================================

......
 pipeline {
    agent any

  stages {
    stage("Initial cleanup") {
          steps {
            dir("${WORKSPACE}") {
              deleteDir()
            }
          }
        }
    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }

    stage('Package'){
      steps {
        script {
          sh 'echo "Packaging App" '
        }
      }
    }

    stage('Deploy'){
      steps {
        script {
          sh 'echo "Deploying to Dev"'
        }
      }

    }
    
    stage("clean Up"){
       steps {
        cleanWs()
     }
    }
     
    }
}

.......
