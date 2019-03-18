node {
   def mvnHome
   def version
 
   stage('Cloning') {
      git 'https://github.com/SeshagiriSriram/addressbook.git'
      mvnHome = tool 'MAVEN_HOME'
          version = '2.3.5'
   }
stage('BUILD')
{
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" clean"/)
      }
}
stage('email')
{
    emailext attachLog: true, body: '', subject: 'yes man', to: 'chahat.nayyar08@gmail.com'
}
}
