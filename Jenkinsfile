def currentBranch = build.environment.get("GIT_BRANCH")
def currentBuildNumber = build.environment.get("BUILD_NUMBER")

def runningBuilds = build.getProject().builds.findAll{ it.getResult().equals(null) }

runningBuilds.each{ e ->
  runningBuildNumber = e.environment.get("BUILD_NUMBER")
  runningBranch = e.environment.get("GIT_BRANCH")

  if( runningBuildNumber != currentBuildNumber && runningBranch == currentBranch ){
    println "interrupted by build #${currentBuildNumber} and Branch ${currentBranch}"
    e.doStop()
  }
}

