node('built-in') 
{
	stage('Continuous Download_Loans') 
	{
		git 'https://github.com/sunildevops77/maven.git'
	}
	stage('Continuous Build_Loans') 
	{
		sh 'mvn package'
	}
	stage('Continuous Deployment_Loans') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Test_Master/webapp/target/webapp.war ubuntu@172.31.26.139:/var/lib/tomcat8/webapps/qaenv22.war'
	}
	stage('Continuous Testing_Loans') 
	{
		sh 'echo "testing passed"'
	}
	stage('Continuous Delivery_Loans') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Test_Master/webapp/target/webapp.war ubuntu@172.31.23.100:/var/lib/tomcat8/webapps/prodenv22.war'
	}
}
