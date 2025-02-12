
def name = "hello"
@Library('utils@main') _
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
            script{
                echo "printing the data from the docker file"
                 a=12 
            }

        }
    }



    stage("accessing the value of docker in anotehr stage"){
        script { 
            println("${a}")
        }
    }

    stage("calling the shared libraries"){
        script{ 
            jenkinsfunction()
        } 

    }
 
  stage("another_branch") { 
    script { 
               println("This is from another branch")
             }  
 
 }



stage("Building another pipeline"){ 
        script { 

 

    
       build job: 'shared-librariespipline', 
                 parameters: [ 
                    string( name:'name',value:"this is from another jenkins it is now building an image in another pipeline" )
          ] 
        
 }  }
    



}					
