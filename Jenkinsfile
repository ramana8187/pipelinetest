node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome = tool name: 'maven2', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('send a mail'){
      mail bcc: '', body: 'hi, jenkins pipeline build success.', cc: '', from: '', replyTo: '', subject: 'jenkins-build', to: 'venkataramana.sriram@gmail.com'
   }
   }
