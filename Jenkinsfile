pipeline {
  agent any
  stages {
    
    stage("Build"){
      steps {
        echo "Build API project using npm build or Bazel if a more advanced build system is needed. Modification"
      }
    }

    stage("Unit and Integration Tests"){
      steps {
        echo "Perform unit tests of the internal components using Jest. Perform overall testing of the API using postman's newman cli tool. A conenction to a database will be needed for intergration tests. "
      }
    }

    stage("Code Analysis"){
      steps {
        echo "Perform code analysis using SonarQube to assess the quality of the codebase and identify any issues or areas of concern."
      }
    }

    stage("Security Scan"){
      steps {
        echo "Perform a security scan using Snyk to identfy any vaunablities and stop them from reaching production, provides information to assist with fixing the identified issues."
      }
    }

    stage("Deploy to Staging"){
      steps {
        echo "Deploy build artifact to a Cloudflare workers staging enviroment using the wrangler cli tool."
      }
    }

    stage("Integration Tests on Staging"){
      steps {
        echo "Run newman api testing on the deployed staging version. Likley also wait for some human testing before moving to production."
      }
    }

    stage("Deploy to Production"){
      steps {
        echo "Deploy build artifact to the Production Cloudflare worker once again using the wrangler cli tool."
      }
    }


    
  }
}
