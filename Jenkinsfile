node {
	properties([
		[$class: 'BuildDiscarderProperty',
			strategy: [$class: 'LogRotator',
			artifactDaysToKeepStr: '',
			artifactNumToKeepStr: '',
			daysToKeepStr: '',
			numToKeepStr: '5']
		],
	pipelineTriggers([
	  	[$class: 'GenericTrigger',
			genericVariables: [
				[expressionType: 'JSONPath', key: 'repository', value: '$.repository'],
				[expressionType: 'JSONPath', key: 'organization', value: '$.organization'],
				[expressionType: 'JSONPath', key: 'sender', value: '$.sender'],
				[expressionType: 'JSONPath', key: 'ref_type', value: '$.ref_type'],
				[expressionType: 'JSONPath', key: 'master_branch', value: '$.master_branch'],
				[expressionType: 'JSONPath', key: 'branch_name', value: 'ref']
			],
			regexpFilterText: '',
			regexpFilterExpression: ''
		]
	])
  ])
	stage('Phase 1') {
		echo 'Hello World!'
	}
	stage('Phase 2') {
		slackSend color: '#439FE0', message: 'This is a test!'
	}
}