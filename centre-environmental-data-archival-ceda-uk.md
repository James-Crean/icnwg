---
layout: default
title: Centre for Environmental Data Archival (CEDA), UK
---
<div id="content" class="column">
    <div class="section">
        <a id="main-content"></a>
        <h1 class="title" id="page-title">
            Centre for Environmental Data Archival (CEDA), UK        
        </h1>
        <div class="region region-content">
            <div id="block-system-main" class="block block-system">
                <div class="content">
                    <div id="node-35" class="node node-book node-full clearfix" about="/content/centre-environmental-data-archival-ceda-uk" typeof="sioc:Item foaf:Document">
                        <span property="dc:title" content="Centre for Environmental Data Archival (CEDA), UK" class="rdf-meta element-hidden"></span><span property="sioc:num_replies" content="0" datatype="xsd:integer" class="rdf-meta element-hidden"></span>
                        <div class="meta submitted">
                            <span property="dc:date dc:created" content="2014-07-10T09:50:36-07:00" datatype="xsd:dateTime" rel="sioc:has_creator">Submitted by <span class="username" xml:lang="" about="/users/mchester" typeof="sioc:UserAccount" property="foaf:name" datatype="">mchester</span> on Thu, 07/10/2014 - 09:50</span>    
                        </div>
                        <div class="content clearfix">
                            <div class="field field-name-body field-type-text-with-summary field-label-hidden">
                                <div class="field-items">
                                    <div class="field-item even" property="content:encoded">
                                        <p>Work undertaken so far at CEDA (or on behalf of CEDA by STFC’s Scientific Computing Department) has been done in parallel with a major infrastructure project, JASMIN (<a href="http://www.jasmin.ac.uk">www.jasmin.ac.uk</a>), which has deployed petascale high-performance storage, virtualization and cloud computing capabilities for environmental science, along with site networking changes. A key part of this has been setting up a “Science DMZ” as part of the JASMIN network: a dedicated “friction-free” zone outside the site firewall. Within this zone, staff have deployed (on 10G-connected physical hosts):<br>
                                            • A perfSONAR node,<br>
                                            • A high-performance FTP server for user access to CEDA archives, and<br>
                                            • A high-performance data transfer server for user (RW) access to collaborative workspace areas.
                                        </p>
                                        <p>With help from ESnet engineers, the perfSONAR host (perfsonar-ph01.jc.rl.ac.uk) is now operating with both packet loss  and throughput  tests. Recent tests have achieved up to 3.8Gbps in throughput tests to some ESnet hosts with 0% packet loss.</p>
                                        <p>Alongside the Science DMZ, in the “standard” infrastructure, are the original service hosts (which the high-performance hosts may replace at some stage). These are hosted as virtual machines within a 10G-connected VMWare virtualization environment. An additional perfSONAR node (a virtual machine) has been deployed alongside these “standard” hosts as representative of that environment.</p>
                                        <p>Further work has concentrated on deploying and testing GridFTP on a test server in the standard infrastructure. Configuration and testing is still ongoing, but once complete will be followed by GridFTP deployment on server(s) in the Science DMZ.</p>
                                        <p>Parts of the project specifically related to ICNWG goals amounts to approximately two staff weeks of system support, plus additional management and other activities. System support effort concentrated on deployment of physical and virtual machines, liaisons with site networking to affect network changes, firewall configuration and interaction with ESnet engineer support. The main challenges for CEDA, to date, have been balancing priorities for staff time against the larger task of constructing and integrating the JASMIN infrastructure, and understanding the perfSONAR configuration (how to set up tests with firewall configurations).</p>
                                        <p>In the next six months to a year, CEDA within the JASMIN infrastructure will<br>
                                            • Monitor and study perfSONAR results to ensure best performance is being achieved<br>
                                            • Deploy GridFTP on existing high-performance data transfer node in Science DMZ<br>
                                            • Set up of data transfer tests with other data centers and test disk-to-disk performance<br>
                                            • Set up of ESGF data node webserver in Science DMZ<br>
                                            • Set up of additional data transfer node for arrivals in Science DMZ (for replication use case, with twin for striped GridFTP use)<br>
                                            • Investigation use of hypervisor in Science DMZ for hosting additional nodes (limited space for physical servers). Includes setup of dedicated hypervisor<br>
                                            • Set up additional perfSONAR tests with other partner sites in UK 
                                        </p>
                                        <p>Setting up a Science DMZ has already shown major (10x) performance benefits in throughput for end user science data transfers (exceeding end-user expectations in capability for data moving).</p>
                                        <p>Understanding long-path network transfers has increased among system support and data center staff, who are now better able to advise users on appropriate transfer methods for particular scenarios.</p>
                                        <p>And some foreseeable challenges looking forward include:<br>
                                            • Expansion of Science DMZ to additional physical hosts may be limited by physical space, hence investigating use of a hypervisor for Science DMZ VMs.<br>
                                            • Set up of additional server for striped GridFTP will likely require additional testing and troubleshooting.<br>
                                            • Contention with a growing community of bandwidth-hungry science data end users (demand growing to meet capacity) is also an ongoing challenge.
                                        </p>
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