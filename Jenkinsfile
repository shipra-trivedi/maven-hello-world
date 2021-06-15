node {

        def mvnHome = tool 'Maven 3'
    stage ("checkout")  {
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Sujana-Suresh/maven-hello-world.git']]])
    }

        stage ('build')  {
    sh "${mvnHome}/bin/mvn clean install -f my-app/pom.xml"
    }
   

      }
