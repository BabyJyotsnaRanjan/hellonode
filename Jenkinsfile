node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("<Docker_ID>/hellonode")
    }

   
    stage('Push image') {
            sh ' docker login -u <Docker_ID> -p <Docker_Password>'
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
       /* }*/
    }
}
