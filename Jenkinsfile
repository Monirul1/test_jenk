def currentBuildNum = currentBuild.number
//find all the runnning builds equals to a currentbranch
def currentBranch = env.BRANCH

//println "${currentBuildNum} and ${currentBranch}"

def runningBuilds = Jenkins.instance.getItem("jenk-pipeline").builds.findAll {it.getResult().equals(null) && currentBranch}

runningBuilds.each{ e ->
  def runningBuildNum = e.number
  if(currentBuildNum != runningBuildNum){
    println "This build was interrupted by the latest build of branch ${currentBranch}"
    e.doKill()
    
  }
}
