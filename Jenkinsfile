@Library('vmn-devops-core') _
testing()
/*
def buildSource(){
  for(i = 0; i < 200000; i++)
  {
    print "."
  }
  
}

def cancelStaleBuilds() {

    stage('Cancel Stale Builds') {
        currentBuildNum = currentBuild.number
        currentBranch = env.BRANCH

        try {
            currentBuild.rawBuild.getParent().builds.each {build ->
                def buildNum = build.number
                def buildBranch = build.getEnvironment().BRANCH

                if (build.isInProgress() && currentBuildNum > buildNum && currentBranch == buildBranch) {
                    println("[cancelStaleBuilds] Build Cancelled: #${buildNum} ${buildBranch}")
                    build.description = "Superseded by build #${currentBuildNum}"
                    build.doKill()
                }
            }
        } catch (NoSuchElementException ex) {
            println('[cancelStaleBuilds] Caught NoSuchElementException. No action needed.')
        } catch (Exception e) {
            println("[cancelStaleBuilds] Caught exception: ${e}")
        }
    }
}
cancelStaleBuilds()
buildSource()
*/


/*currentBuildNum = currentBuild.number
currentBranch = env.BRANCH

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
    
  }
  catch(NoSuchElementException ex){
      println "Caught NoSuchElementException, expected behavior."
  }

}

cancelOldBuilds()
buildSource()
*/
