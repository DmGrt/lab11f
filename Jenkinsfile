pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh "mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args="'1628437518:AAHkDppuffbvv3g9ATXSlXa4N83iD-xBSA0' 'laberman_bot'""
            }
        }
    }
}