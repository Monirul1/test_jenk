def currentBuildNum = currentBuild.number
//find all the runnning builds equals to a currentbranch
def currentBranch = env.BRANCH

//println "${currentBuildNum} and ${currentBranch}"

def runningBuilds = currentBuild.rawBuild.getParent().builds.each{ e ->
  
  def runningBuildNum = e.number
  
  if(e.getResult().equals(null) && currentBranch && currentBuildNum != runningBuildNum){
    
    println "This build was interrupted by the latest build of branch ${currentBranch}"
    e.doKill()
  }
  
}
