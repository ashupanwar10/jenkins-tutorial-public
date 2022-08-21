pipeline {
  agent any

  parameters {
    string(name: 'Greeting', defaultValue: 'Hello', description: "How should I greet the world?")
  }
  stages {
    stage("Example"){
      steps{
        echo "${params.Greeting} World!"
      }
    }
  }
}

/*
Hello Everyone

Welcome to Coding Bug. In today's video we will see how we can use the parameters in any declarative pipline

To demonstrate this I am using VScode to write the pipeline job than we will copy the code to Jenkins.


So Let's get started with writing our JOB.

First, let's open the vscode and create one Jenkinsfile, 

Once you create the Jenkinsfile declare the pipeline block as we are creating the declarative pipeline  here

after pipeline declaration we will define agent as any, it means job can run on any agent

now lets start with stages first, stages, than stage , let 's call it hello, inside the hello stage we will define our steps

in this job we are using only one step which is to print hello with name of a persone which we will be defining in parameters

so step will be echo "Hello" and some "Name"

now we will see how we can define the parameters, got to top inside the pipline we will define parameters block.

inside the parameters block as name is a string we will define string type parameter.

name will be the name of variable, in our case let;s call it userName then default value what ever we want to define lets call it 
Mr. Bob and then description: Let say "user who will trigger the job"

so we have created the paramaters, now the question is how we call call this in our steps. to call the variable in steps we will use 
interpolation

so let's go to the steps section and call the parameter. to call the paramters we will start with ${} and inside the brakets 
params.userName

Now lets go to Jenkins and create a new pipelineJOB, copy the code and paste it to pipeline defination section

apply the changes and save. now let's run the job.

it will ask you for paramters value while exution but you can ignore and run with default value

job has been executed successfully

let check the logs now, as you can see we have hello and the userName printed in this console.

This is how we can use the parameters in jenkins pipeline

Hope this video was informative for you, thanks for watching, see you in upcomning videos.

*/