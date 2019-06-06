pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn -f mavewebappdemo/pom.xml install'
                
            }
        }

        stage('Deploy to Tomcat'){
        steps {
        sh 'cp -r /root/.jenkins/jobs/pipeline2/workspace/mavewebappdemo/target/* /opt/apache-tomcat-8.0.29/webapps/'
        }
        }


        
    }
}
