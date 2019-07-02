
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

def cancelOldBuilds() { currentBuild.rawBuild.getParent().builds.each{ e ->

  try {
    def runningBuildNum = e.number
    def runningBuildBranch = e.getEnvironment().BRANCH

    println "Iterating over all builds"
    if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
      println "Assigning buildnum ${runningBuildNum}"
      println "Assigning branch ${runningBuildBranch}"
      e.doKill()

    }
  } catch(Exception e) {

    println "cathing"

  }

}

}

println "calling the method caneloldbuild"
cancelOldBuilds()


// to run
buildSource()



