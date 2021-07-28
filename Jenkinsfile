node('MASTER')
{
    stage('SCM'){
        git 'https://github.com/sirikodali/openmrs-core.git'
    }
    stage('BUILD'){
        sh 'mvn package'

    }
    stage('Post'){
        archive '**/*.war'
        junit '**/TEST-*xml'
    }
}
