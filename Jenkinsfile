config {
	daysToKeep = 21
	cronTrigger = '@weekend'
}

node() {
   	git.checkout { }

	def img = dockerfile.build {
		name = 'selenium-chromium-headless'
	}

	dockerfile.publish {
		registry = 'docker.topicusonderwijs.nl'
   		image = img
	   	baseTag = false
    }
}
