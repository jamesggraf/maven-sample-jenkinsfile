stage 'clean'
node {
  checkout scm
  sh "git status"
  //def mvnHome = tool 'M3'
  //sh "${mvnHome}/bin/mvn -B verify"
  sh "mvn -B clean"
  sh "git log"
  sh "git status"
}

stage 'verify'
node {
  sh "mvn -B verify"
}

stage 'approve'
input message: 'Do you want to deploy?'

stage 'deploy'

node {
  echo 'Deploying'
}
