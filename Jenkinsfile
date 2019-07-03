
//  currentBuildNum = currentBuild.number
//currentBranch = env.BRANCH
// builsource will run continuosly
currentBuildNum = currentBuild.number
currentBranch = env.BRANCH

println "getting buildSource"
def buildSource(){
  for(i = 0; i < 200000; i++)
  {
    print "."
  }

}

def cancelOldBuilds() { 
  
  try {
    currentBuild.rawBuild.getParent().builds.each{ e ->
        def runningBuildNum = e.number
        def runningBuildBranch = e.getEnvironment().BRANCH

    println "Iterating over all builds"
    if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
      e.doKill()

    }
  } 
    catch(Exception ex) {
    println "HEJHFBERHJBGHJERBGHJBGJR"
    println ex.getMessage()
          

  }

}

}

println "calling the method caneloldbuild"
cancelOldBuilds()


// to run
buildSource()




