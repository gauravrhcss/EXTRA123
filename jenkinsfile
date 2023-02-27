pipeline {
    agent any

    stages {
        stage('Download Data from github accout') {
            steps {
                git 'https://github.com/gauravrhcss/BADBOY.git'
            }
        }
    stage('Transfer data from jenkins to ansible machine') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'jenkins', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'rsync -e "ssh -p 225" /var/lib/jenkins/workspace/first-pipeline/* root@101.53.148.193:/var/www/html', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
        
    }
}
