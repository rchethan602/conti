pipeline {
    agent any

    parameters {
        choice(name: 'REGION', choices: ['eu-central-1','us-east-1', 'cn-north-1'], description: 'Target AWS region')
        choice(name: 'PROJECT_NAME', choices: ['fcs', 'keycore'], description: 'Target application')
        choice(name: 'NAMESPACE', choices: ['yosemite','sequoia','whiskeytown','demo','honda-sandbox','preprod','sandbox','demo','ioptesting','nissan-sandbox','preprod','rosie','santa-monica','preprod','wutai','qiyun','preprod','putuo'], description: 'Target namespace on the environment')
        choice(name: 'DB_TYPE', choices: ['mongo', 'psql'], description: 'Target database type')
        string(name: 'VERSION', defaultValue: 'master', description: 'Git sha1, git tag or git branch for csmrck-backend repository. This is used to checkout the Jenkins pipeline code ')
    }
	
	
    stages(deploy) {
        stage(Checking) {
            steps {
				script {
					sh "echo testing pipeline script "
				}
            } 
        }
    }
}
