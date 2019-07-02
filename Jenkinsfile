def currentBuildNum = currentBuild.number
//find all the runnning builds equals to a currentbranch
def currentBranch = env.BRANCH

def foreverLoop(){
    for(i = 0; i < 200000; i++)
  {
    print "."
  }

}

println "beofre iterate"
currentBuild.rawBuild.getParent().builds.each{ e ->

  println "Assigning runningbuildnum"
  def runningBuildNum = e.number
  println "Assigning runningbuildbranch"
  def runningBuildBranch = e.getEnvironment().BRANCH
  println "Iterating over all builds"
  if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
    println "killingbuilds"
    e.doKill()
     println "donee"
  } else if(e.getResult().equals(null) && currentBuildNum == runningBuildNum && currentBranch == runningBuildBranch)
  {
      foreverLoop()
  }
     
}
