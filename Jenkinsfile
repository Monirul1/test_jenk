
//  currentBuildNum = currentBuild.number
//currentBranch = env.BRANCH
// builsource will run continuosly

def currentBuildNum = currentBuild.number
def currentBranch = env.BRANCH

println "getting buildSource"
def buildSource(){
  for(i = 0; i < 200000; i++)
  {
    print "."
  }
  
}

def cancelOldBuild() { currentBuild.rawBuild.getParent().builds.each{ e ->
  
  def runningBuildNum = e.number
  println "Assigning buildnum ${runningbuildnum}"
  def runningBuildBranch = e.getEnvironment().BRANCH
  println "Assigning branch ${runningbuildbranch}"
  println "Iterating over all builds"
  if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
    
    e.doKill()
    
  }
  
}

}

println "calling the method caneloldbuild"
cancelOldBuild()

// to run
currentBuild.rawBuild.getParent().builds.each{ e ->
  //println "Assigning runningbuildnum"
  def runningBuildNum = e.number
  //println "Assigning runningbuildbranch"
  def runningBuildBranch = e.getEnvironment().BRANCH
  //println "Iterating over all builds"
  if(e.getResult().equals(null) && currentBuildNum == runningBuildNum && currentBranch == runningBuildBranch){
    
    buildSource()
    
  }
  
}
