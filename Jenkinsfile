currentBuildNum = currentBuild.number
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
        println "Assigning buildnum ${runningBuildNum}"
        println "Assigning branch ${runningBuildBranch}"
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
