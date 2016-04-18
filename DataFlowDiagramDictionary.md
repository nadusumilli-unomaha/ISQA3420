#Data Flow Diagram Dictionary

##Entities<br/>
**Corporate Developer:** - Executes a wide range of business strategies to meet organizational requirements.<br/>
**Corporate Manager:** - Leads, administers and directs a company.<br/>
**NIST National Vulnerability Database** - Database maintained by NIST which catalogs discovered vulnerabilities in software packages<br/>

##DataFlows<br/>
**CPE Request** - A query from a cron job to request NIST CPE information.<br/>
**CPE Response:** - CPE file response from NIST.<br/>
**CPE File** - Processed CPE file from NIST.<br/>
**Software CPE Query** - Query from Compare File and Package to NIST CPE process to NIST CPE Information datastore.<br/>
**Software CPE Response** - Results from Software CPE Query to NIST CPE Information datastore.<br/>
**File Information** - Request query from Corporate Developer to Compare File and Package to NIST CPE process soliciting information on a particular file.<br/>
**Package Information** - Request query from Corporate Developer to Compare File and Package to NIST CPE proceess soliciting information on a particular package.<br/>
**Compared CPE Response** - Response from Compare File and Package to NIST CPE process to Corporate Developer following File Information or Package Information query.<br/>
**CPE Information** - Input to update Software Manifest by Corporate Developer to Manage Software Manifest process.<br/>
**Request Manifest** - Query from Corporate Developer to Manage Software Manifest process to retrieve current manifiest information.<br/>
**Manifest Information** - Response data from Manage Software Manifest process to Corporate Developer following Request Manifest query.<br/>
**Sorted CPE Information** - Processed CPE Information from Manage Software Manifest process to be added to Software Manifest datastore.<br/>
**Manifest Info Query** - Query from Manage Software Manifest process to Software Manifest datastore to retrieve current manifest information.<br/>
**Manifest Query Return** - Response from Software Manifest Datastore to Manage Software Manifest process with current manifest information.<br/>
**Package and CPE Information** - Processed package and CPE information for current file or package to be stored in Risk Database.<br/>
**Package Information Request** - Query from Manage Project Information process to Risk Database datastore to retireve current risk information.<br/>
**Package Information Response** - Return information from Risk Database following query for current risk information.<br/>
**Package Info Request** - Request from Corporate Manager to Manage Project Information process for current risk information.<br/>
**Package Info Response** - Return information from Manage Project Information process to Corporate Manager with current risk information.<br/>
**Update Policy** - Input from Corporate Manager to Update Policy Documents process to update stored policy.<br/>
**Request Policy** - Input from Corporate Manager to retrieve current policy documents from Manage Policy Documents process.<br/>
**Policy Information** - Return from Manage Policy Documents process to Corporate Manager with current policy information.<br/>
**Updated Policy Info** - Query from Manage Policy Documents process to Policy Database to update stored policy information.<br/>
**Current Policy Info** - Response from Policy Database datastore with current policy information to Manage Policy Documents process.<br/>

##DataStores<br/>
**NIST CPE Information** - Stores retrieved CPE information provided by NIST and also current package and file information for code used used by organization in software development.<br/>
**Policy Database** - Stores organizational policies on acceptable risk levels and handling procedures for code used in development.<br/>
**Risk DB** - Stores file and package CPE information used by the organization in software development including current assessed risk levels.<br/>
**Software Manifest** - Stores and catalogs all file and package information in use in individual software projects.<br/>

##Processes<br/>
**Compare File and Package to NIST CPE** - Receives file and package information from the developer and current CPE information from NIST CPE Database. Processes and organizes results to send the results to the developer and to update the Risk DB.<br/>
**Manage Software Manifest** - Processes and organizes the CPE Information and currently used files and packages  and sends it to the software Manifest datastore.<br/>
**Manage CPE Information** - Cron job which gathers CPE information on a daily basis from NIST and stores in the NIST CPE Information datastore.<br/>
**Manage Project Information** - Processes requests from Corporate Manager for current information stored in Risk DB datastore.<br/>
**Manage Policy Documents** - Process to update and retrieve policy information stored in the Policy Database datastore.<br/>
