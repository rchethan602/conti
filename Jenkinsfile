#!groovy
pipeline {
	agent any
    stages {
        stage("Create KAAS pipelines for cleaning and deploying components") {
            steps {
                jobDsl scriptText: """
                    pipelineJob("db-support-scripts") {
                        definition {
                            cpsScm {
                                scm {
                                    git {
                                        branch('main')
                                        remote {
                                            name('origin')
                                            url('git@github.com:rchethan602/conti.git')
                                        }
                                        extensions {
                                            wipeOutWorkspace()
                                        }
                                    }
                                }
                                scriptPath('Jenkinsfile.db')
                            }
                        }
                    }
				"""
			}
        }
    }
}
