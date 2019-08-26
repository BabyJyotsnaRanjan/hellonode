node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("jyotsna25ranjan/hellonode")
    }

   
    stage('Push image') {
            sh ' docker login -u jyotsna25ranjan -p Welcome@123'
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
       /* }*/
    }
}
