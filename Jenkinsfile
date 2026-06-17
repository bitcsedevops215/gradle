pipeline{
	agent any
	tool{
		gradle'Gradle'
		jdk'JDK'
		}
	stages{
		stage('checkout'){
			steps{
			git branch:'master'url:'https://github.com/bitcsedevops215/gradle.git'
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
		stage('build'){
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
