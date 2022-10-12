node{
      def mvnHome = tool name: "maven_3.8.4"
  // clone the code from SCM;github
  stage("cloning"){
    git credentialsId: '19127c07-7e12-4694-a7b4-fba271c0d208', url: 'https://github.com/mgmmourya/maven-web-application.git'
  }
  // creating the package
    stage("build"){
    sh "$mvnHome/bin/mvn clean package"
  }
   /* //generating the sonarqube report
    stage("SonarReport"){
      sh "$mvnHome/bin/mvn sonar:sonar"
    }
     //uploading the artifacts into artifact repo
    stage("Uploading artifacts"){
      sh "$mvnHome/bin/mvn deploy"
    }
  //deploying the application into tomcat
    stage("Deploy"){
      sshagent(['838ac8d1-b10a-440b-9116-7ee44bf89ec1']){
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.6.126.248:/opt/tomcat/webapps"
}
    } */
}
