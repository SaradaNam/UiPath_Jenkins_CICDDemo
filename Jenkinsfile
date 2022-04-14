pipeline {
	    agent any
	
	        // Environment Variables
	        environment {
	        MAJOR = '1'
	        MINOR = '0'
	        //Orchestrator Services
	        UIPATH_ORCH_URL = "https://cloud.uipath.com/"
	        UIPATH_ORCH_LOGICAL_NAME = "saradanamburi"
	        UIPATH_ORCH_TENANT_NAME = "saradanamburi"
	        UIPATH_ORCH_FOLDER_NAME = "Shared"
	    }
 stages {
    stage ('Build') {
        UiPathRunJob(
          credentials: UserPass('_9k5cK9oUpE2ER4M2VrpsLMPBDorlAudUZRlcG61xGhcH'),
          failWhenJobFails: true,
          folderName: 'Shared',
          orchestratorAddress: 'https://cloud.uipath.com/',
          orchestratorTenant: 'saradanamburi',
          parametersFilePath: '',
          priority: 'Low',
          processName: 'UiPath Jenkins CICD Demo',
          resultFilePath: 'output.json',
          strategy: Dynamically(jobsCount: 1, machine: 'TestMachine', user: 'TestUser'), timeout: 3600, waitForJobCompletion: true, traceLoggingLevel: 'None'
        )
        UiPathRunJob(
          credentials: UserPass('_9k5cK9oUpE2ER4M2VrpsLMPBDorlAudUZRlcG61xGhcH'),
          failWhenJobFails: true,
          folderName: 'Shared',
          orchestratorAddress: 'https://cloud.uipath.com/',
          orchestratorTenant: 'saradanamburi',
          parametersFilePath: '',
          priority: 'Low',
          processName: 'UiPath Jenkins CICD Demo',
          resultFilePath: 'output.json',
          strategy: Robot('robot1,robot2'),
          timeout: 1800,
          waitForJobCompletion: false,
          traceLoggingLevel: 'None'
        )
    }
