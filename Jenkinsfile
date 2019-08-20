node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("prabeesh/hellonode")
    }

   
    stage('Push image') {
            sh ' docker login -u prabeesh -p Mindtree@2019'
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
       /* }*/
    }
}
