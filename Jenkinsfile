import hudson.model.AbstractModelObject
import hudson.model.Actionable
import hudson.model.Result

import hudson.model.AbstractItem
import hudson.model.Job
import hudson.model.AbstractProject
import hudson.model.Project
import hudson.model.*
import hudson.model.Run
//import jenkins.model.*
jenkins = Jenkins.instance

//def runningBuilds = Jenkins.instance.getProjects("jenk-pipeline")
def currentBuildNum = currentBuild.number
//find all the runnning builds equals to a currentbranch
def currentBranch = env.BRANCH
//println currentBuild

def runningBuilds = Jenkins.instance.getItem("jenk-pipeline").builds.findAll {it.getResult().equals(null) && currentBranch}


runningBuilds.each{ e ->
  def runningBuildNum = e.number
  if(currentBuildNum != runningBuildNum){
    e.doStop()
    
  }
}
