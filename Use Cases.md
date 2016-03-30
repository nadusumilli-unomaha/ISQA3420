#Use Cases
##Use Case 1
__Title__: Determine License and Vulnerability Information<br/>
__Primary Actor__: Corporate Manager<br/>
__Goal in Context__: The corporate manager is able to determine license and vulnerability information from provided project information<br/>
__Stakeholders__: <br/>
  Corporate Manager: To receive clear and relevant project information<br/>
  Corporate Developer: To provide the relevant file/package level information<br/> 
  Project Owner: To clearly understand corporate manager decisions to green/red light a project <br/>
__Preconditions__:<br/>
  Relevant file/package information is in the SPDX database<br/>
  Proper project information has been provided  <br/>
__Main Success Scenario__: Corporate manager receives accurate license and vulnerability information for the requested project packages<br/>
__Failed End Conditions__: Corporate manager receives inaccurate or invalid license and vulnerability information for the requested project packages<br/>
__Trigger__: Corporate manager uploads or identifies project information to which license and vulnerability information is provided<br/>

##Use Case 2
__Title__: Enter Package and File CPE Data<br/>
__Primary Actor__: Corporate Developer<br/>
__Goal in Context__: The corporate developer is able to update risk database with new software package CPE and file CPE data following comparison to NIST CPE information from vulnerability database.<br/>
__Stakeholders__: <br/>
  Corporate Manager: To maintain up-to-date file and package information stored in risk database concerning software in development.<br/>
  Corporate Developer: To provide the processed comparison results to NIST vulnerability data.<br/> 
  Project Owner: To be aware of current known risks involved with the use of open source software in the project.<br/>
__Preconditions__:<br/>
  Current CPE data from NIST is in NIST CPE repository.<br/>
  Accurate file and package information is entered by developer.<br/>
__Main Success Scenario__: Risk database is updated with file/package information with known vulnerabilities highlighted to compare to policy information in policy database and perform risk assessment.<br/>
__Failed End Conditions__: Risk database is updated with inaccurate or incomplete vulnerability information for the project packages and files in use.<br/>
__Trigger__: Software Developer uploads file and package information for comparison with NIST CPE repository.<br/>

##Use Case 3
__Title__: Check Vulnerabilities Against Policy<br/>
__Primary Actor__: Corporate Manager<br/>
__Goal in Context__: The corporate manager is able to compare risk assessment results of package and file information stored in the risk database with policy documents defining acceptable risk levels.<br/>
__Stakeholders__: <br/>
  Corporate Manager: To objectively assess risk levels of open source software in use in project under development and enforce use policies impartially.<br/>
  Corporate Developer: To utilize open source software to develop software project which reach goals without placing the company or its data at risk.<br/> 
  Project Owner: To protect company assets from exploitation from outside sources and maintain compliance with licensing rules.<br/>
__Preconditions__:<br/>
  Policy information must be clear and up-to-date.<br/>
  Accurately risk-assessed software and package information in risk database.<br/>
__Main Success Scenario__: Software which meets vulnerability requirements is deployed while open source software which does not meet acceptable risk levels will be rejected and alternatives will be employed.<br/>
__Failed End Conditions__: Risk information or policy information is innaccurate causing excessively risky open source software to be utilized or license terms not met.<br/>
__Trigger__: Corporate manager queries both risk database and policy database to compare current packages and files vulnerability results with policy.<br/>
