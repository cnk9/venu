node {
      stage ('git clone'){
	  git credentialsId: 'github_root',url:'https://github.com/cnk9/cnkgit.git'
	  }
	  stage('clean'){
	  sh 'mvn clean'
	  }
	  stage('code scan'){
	  sh 'mvn sonar:sonar \
	   -Dsonar.host.url=http://35.226.143.202:9000 \
	   -Dsonar.login=204b7350cdb78f81cb29fe65927e83d64c1377d8'
	   }
	  stage('compile'){
	  sh 'mvn compile'
	  }
	  stage('package'){
	  sh 'mvn package'
	  }
	  stage('deploy'){
	  sh 'mvn deploy'
	  }
	  }
