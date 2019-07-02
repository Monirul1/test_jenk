def currentBuildNum = currentBuild.number
def currentBranch = env.BRANCH

def buildSource(){
    for(i = 0; i < 200000; i++)
  {
    print "."
  }

}


 def cancelOldBuids() {currentBuild.rawBuild.getParent().builds.each{ e ->

  //println "Assigning runningbuildnum"
  def runningBuildNum = e.number
  //println "Assigning runningbuildbranch"
  def runningBuildBranch = e.getEnvironment().BRANCH
  //println "Iterating over all builds"
  if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
   
      e.doKill()
      
  }
     
}
                       
 }
                      
 


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


                

