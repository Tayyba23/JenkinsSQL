node {
    // Clean workspace before doing anything
  

    try {
        stage ('Clone') {
            checkout scm
            
        }
        stage ('Build') {
            bat "test.bat"
        }
        stage ('Tests') {
            
            'unit': {
                //call taf , add atleast 10 tables
                bat "echo 'shell scripts to run unit tests...'"
            },
            
        }
        stage ('Deploy') {
            //update dashboard
            bat "echo 'shell scripts to deploy to server...'"
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}
