pipeline {
    agent {
        docker {
            image: 'quay.io/lineageos/builder_android'
            label: 'phenom'
            args: '-v /lineage:/lineage -v /ccache:/ccache'
        }
    }
    stages {
        stage("sync") {
            dir("/lineage/cm-14.1"){
                sh "repo sync"
            }
        }
    }
}
