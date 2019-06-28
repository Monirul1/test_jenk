import hudson.model.AbstractModelObject
import hudson.model.Actionable

import hudson.model.AbstractItem
import hudson.model.Job
import hudson.model.AbstractProject
import hudson.model.Project
import hudson.model.*
import hudson.model.Run 
//import jenkins.model.*
jenkins = Jenkins.instance

 //def runningBuilds = Jenkins.instance.getProjects("jenk-pipeline")
 def runningBuilds = Jenkins.instance.getItem("jenk-pipeline").builds.findAll { it.getResult().equals(null) }

runningBuilds.each{ e ->
     
     if(env.BRANCH == "master"){
            //print latest running build within this branch
      println  "RUNNINGGGG ${runningBuild}"

}
}



/*
def branch = env.BRANCH
 println branch




runningBuilds.each{ e ->
     
     if(e.environment.get("GIT_BRANCH") == "origin/master"){
            //print latest running build within this branch
      println  "RUNNINGGGG ${runningBuild}"

}
}
*/
