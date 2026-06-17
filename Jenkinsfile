pipeline{
	agent any
	tools{
		gradle'Gradle'
		jdk'JDK'
		}
	stages{
		stage('checkout'){
			steps{
			git branch:'master'url:'https://github.com/bitcsedevops215/gradle'
			}
		}
		stage('test'){
			steps{
			sh'gradle test'
			}
		}
		stage('build'){
			steps{
			sh'gradle build'
			}
		}
		stage('run'){
			steps{
			sh'gradle run'
			}
		}
		}
	post{
		success{
			echo'build and deployment successful!'
			}
		failure{
			echo'build failure'
			}
		}
	}
