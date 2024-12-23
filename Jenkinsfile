pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment {
    PATH = "/opt/apache-maven-3.9.9/bin:$PATH"
}

    stages {

       /* stage ('cloneproject')
        {
            steps{

                echo "-----clone the project"
                git branch: 'master', url: 'https://github.com/venkymca/devops-test-project.git'
            }
        } */
        stage("build"){
            steps {
                 echo "----------- build started ----------"
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                 echo "----------- build complted ----------"
            }
        }
    }

}  
