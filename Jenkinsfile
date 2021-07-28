node('GOL')
{
    stage('SCM'){
        git 'https://github.com/sirikodali/openmrs-core.git'
    }
    stage('BUILD'){
        sh 'mvn clean package'

    }
    stage('Post'){
        junit '**/*.war'
        archive '**/TEST-*xml'
    }
}
