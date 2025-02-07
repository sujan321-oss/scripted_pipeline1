
def name = "hello"

node {
    def KEY_IMAGE = "ubuntu:latest" 
    stage("building an image") { 

        script{
            println("building an image")
        }
         
    }

    stage("run inside the docker"){
        docker.image(KEY_IMAGE).pull()
        docker.image(KEY_IMAGE).inside{
            sleep(20)
            script{
                echo "printing the data from the docker file"
            }

        }
    }



}
