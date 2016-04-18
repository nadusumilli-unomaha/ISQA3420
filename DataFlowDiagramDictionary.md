#Data Flow Diagram Dictionary
##Entities<br/>
**Corporate Developer:** Executes a wide range of business strategies to meet organizational requirements.<br/>
**Corporate Manager:** Leads, administers and directs a company.<br/>
**National Vulnerability Database** - include databases of security checklist<br/>

##DataFlows<br/>
**CPE Information:** Unique Identifier for software package.<br/>
**CPE Response:** Retreiving licensing information.<br/>
**CPE Request** - A request for license information.<br/>

##DataStores<br/>
**NIST National Vulnerability Database:** Include all the information of the security checklist in a database.<br/>
**Policy Database:** Includes all the policy information that is used for managing external source in a database.<br/>
**Risk DB** - software package data exchange, to create repositories of articles to capture and share community knowledge.<br/>
**Software Maniferst** Includes information relating to the project for downstream developers.<br/>

##Processes<br/>
**Compare File and Package to NIST CPE:** Recieves the File and Package information from the developer and sends it to the NIST database and then send the results to the developer and the risk DB.<br/>
**Manage Software Manifest:** Gets the CPE Information and sorts the information in order to send it to the software manifest DB.<br/>
**Manage CPE Information** Gathers CPE informaiton on a daily basis and stores them in the NIST CPE Information.<br/>
**Manage Project Information** Makes a request for package informaiton and passes it to the corporate manager.<br/>
**Manage Policy Information** Queries policy information and add any changes make to the policy document.<br/>
