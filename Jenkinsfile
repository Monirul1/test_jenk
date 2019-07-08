def buildSource(){
  for(i = 0; i < 200000; i++)
  {
    print "."
  }
  
}

def cancelStaleBuilds() {

  println("Checking for stale builds...")
  currentBuildNum = currentBuild.number
  currentBranch = env.BRANCH

  try {
    currentBuild.rawBuild.getParent().builds.each{ e ->
      def runningBuildNum = e.number
      def runningBuildBranch = e.getEnvironment().BRANCH

      if(e.getResult().equals(null) && currentBuildNum != runningBuildNum && currentBranch == runningBuildBranch){
        println("Build #${runningBuildNum} building ${runningBuildBranch} was cancelled")
         e.doKill()
      }
    }
  } catch(NoSuchElementException ex){
     println("Caught NoSuchElementException, expected behavior. No action needed.")
  } catch(Exception x){
     println("X was caught")
  }
  println("Finished checking for stale builds.")
}
cancelStaleBuilds()
buildSource()


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
