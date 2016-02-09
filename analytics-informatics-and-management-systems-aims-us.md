---
layout: default
title: Analytics, Informatics, and Management Systems (AIMS), US
---
<div id="content" class="column">
    <div class="section">
        <a id="main-content"></a>
        <h1 class="title" id="page-title">
            Analytics, Informatics, and Management Systems (AIMS), US        
        </h1>
        <div class="region region-content">
            <div id="block-system-main" class="block block-system">
                <div class="content">
                    <div id="node-39" class="node node-book node-full clearfix" about="/content/analytics-informatics-and-management-systems-aims-us" typeof="sioc:Item foaf:Document">
                        <span property="dc:title" content="Analytics, Informatics, and Management Systems (AIMS), US" class="rdf-meta element-hidden"></span><span property="sioc:num_replies" content="0" datatype="xsd:integer" class="rdf-meta element-hidden"></span>
                        <div class="meta submitted">
                            <span property="dc:date dc:created" content="2014-07-10T09:51:53-07:00" datatype="xsd:dateTime" rel="sioc:has_creator">Submitted by <span class="username" xml:lang="" about="/users/mchester" typeof="sioc:UserAccount" property="foaf:name" datatype="">mchester</span> on Thu, 07/10/2014 - 09:51</span>    
                        </div>
                        <div class="content clearfix">
                            <div class="field field-name-body field-type-text-with-summary field-label-hidden">
                                <div class="field-items">
                                    <div class="field-item even" property="content:encoded">
                                        <p>Over the past few months AIMS personnel have performed a general investigation into the optimal virtual machine networking configurations, comparing SR-IOV versus VirtIO; this has shown that SR-IOV is superior in maxing out throughput using Infiniband (IB) and 10GE cards in a virtual machine (VM) environment. In addition, AIMS has completed and received approval for security policy changes required to deploy data transfer node (DTN) systems. They have configured a pair of hypervisors and 10 virtual machines to serve as the DTN cluster. Basic GridFTP transfers have been demonstrated and the process of configuring the system for production use has begun. The connection from the LLNL Science DMZ to ESnet is in the process of being upgraded to 100Gbps from 10Gbps.  This upgrade is expected to be completed and the new infrastructure put into production in early 2015.  This will significantly increase the network capacity available for data transfers between the AIMS data center and the other climate data centers.</p>
                                        <p>The required resources for AIMS to participate in the project include hiring a new system administrator in Livermore Computing (LC) to provide support on a part-time basis for the deployment of the DTN environment. This took several months for the interviewing, hiring, and training process. AIMS has spent approximately two person-months completing initial benchmarking, hardware acquisition, installation, requirements gathering, research, and configuration. </p>
                                        <p>The LC team has been assisting in this project as well. They have completed the initial deployment of a DTN VM cluster and have demonstrated a 500+ MB/s disk-to-disk transfer rate between data centers. The transfer rates were achieved with GridFTP using eight concurrent copies spread across four Lawrence Livermore National Laboratory’s (LLNL) DTN nodes, with each copy using four threads. The rate to NERSC's General Parallel File System (GPFS) scratch directory on the NERSC DTNs averaged around 520 MB/s. Per the details in Appendix B, achieving this transfer rate in August was a key project milestone. The LC staff used the National Energy Research Scientific Computing (NERSC) Center’s DTN server as their test remote destination because other ICNWG sites were not up yet.</p>
                                        <p>Setting up, configuring, debugging, and fine-tuning the DTN system was a major effort, with significant contributions from LC's System Administration Group, Networking Team, and Advanced Technology Office (ATO). AIMS and the LC team are still in the process of finding the optimal configuration for the climate DTNs, and experts from ATO are working towards a solution that will best meet the long-term needs of the project. </p>
                                        <p>Technical and administrative challenges for working on this project include:<br>
                                            • Finding detailed information about the appropriate configuration of a DTN.<br>
                                            • Determining the virtual machine toolkit best suited for the needs of our DTN environment.<br>
                                            • Implementing security policy changes to accommodate project needs.
                                        </p>
                                        <p>In the next 6 months, AIMS will extend the general VM network evaluation into the specific DTN environment. Globus and/or GridFTP servers will be set-up on the DTNs for external use. AIMS staff will perform extensive benchmarking to measure the effects of virtual machines and different network configurations. In addition, they will configure a VM environment to meet the disk-to-disk bandwidth requirements.</p>
                                        <p>The design of the data storage system may need to be altered in order to meet the longer-term stretch bandwidth goals. Incorporating a parallel file system may be required if AIMS staff find NFS performance to be inadequate.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>