node('built-in') 
{
	stage('Continuous Download_Master') 
	{
		git 'https://github.com/sunildevops77/maven.git'
	}
	stage('Continuous Build_Master') 
	{
		sh 'mvn package'
	}
	stage('Continuous Deployment_Master') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Test_Master/webapp/target/webapp.war ubuntu@172.31.26.139:/var/lib/tomcat8/webapps/qaenv2.war'
	}
	stage('Continuous Testing_Master') 
	{
		sh 'echo "testing passed"'
	}
	stage('Continuous Delivery_Master') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Test_Master/webapp/target/webapp.war ubuntu@172.31.23.100:/var/lib/tomcat8/webapps/prodenv2.war'
	}
}
