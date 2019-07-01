def currentBuildNum = currentBuild.number
//find all the runnning builds equals to a currentbranch
def currentBranch = env.BRANCH

def runningBuilds = currentBuild.rawBuild.getParent().builds.each{ e ->

  def runningBuildNum = e.number
  def runningBuildBranch = e.getEnvironment().BRANCH
  
  if(e.getResult().equals(null) && currentBranch == runningBuildBranch && currentBuildNum != runningBuildNum){

//    e.doKill()
     sleep 40000
    
  } 
  
  
}
