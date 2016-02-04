---
layout: default
title: Data Transfer Nodes
group: "navigation"
weight: 3
---

<div id="content" class="column">
    <div class="section">
        <a id="main-content"></a>
        <h1 class="title" id="page-title">
            Data Transfer Nodes        
        </h1>
        <div class="region region-content">
            <div id="block-system-main" class="block block-system">
                <div class="content">
                    <div id="node-6" class="node node-page node-full clearfix" about="/node/6" typeof="foaf:Document">
                        <span property="dc:title" content="Data Transfer Nodes" class="rdf-meta element-hidden"></span><span property="sioc:num_replies" content="0" datatype="xsd:integer" class="rdf-meta element-hidden"></span>
                        <div class="content clearfix">
                            <div class="field field-name-body field-type-text-with-summary field-label-hidden">
                                <div class="field-items">
                                    <div class="field-item even" property="content:encoded">
                                        <p><a href="http://fasterdata.es.net/science-dmz/DTN/">Data transfer nodes (DTNs)</a> are dedicated, high performing servers used specifically for data transfers. These servers are optimized for large-scale data transfers and are usually best located within a <a href="http://fasterdata.es.net/science-dmz/">Science DMZ</a> infrastructure.</p>
                                        <p>For DTN hardware, LLNL's Livermore Computing Center has compiled a <a href="{{site.baseurl}}/LLNL-HardwareRecommendationsforDTNnodes-150129.pdf">document detailing hardware recommendations </a>  that work well for an ESGF environment.</p>
                                        <p>ICNWG will be working with Globus-equipped DTNs (GridFTP-based software) for data replication between the ESGF sites. LLNL has installed the Globus Connect Server on their DTNs: <a href="{{site.baseurl}}/GlobusConnectServerInstall-llnl_0.pdf">information on how they configured the systems are available here. </a></p>
                                        <hr>
                                        <p>ESnet has three high-performance data transfer hosts connected directly to the ESnet 100Gbps network backbone, which will help test the transfer performance from disk-to-disk for the Globus DTN endpoints.  These are accessible to any university or science site.</p>
                                        <p>-anl-diskpt1.es.net / anl-diskpt1-v6.es.net: Near Chicago, IL<br>
                                            -bnl-diskpt1.es.net / bnl-diskpt1-v6.es.net: Near NYC, NY<br>
                                            -lbl-diskpt1.es.net / lbl-diskpt1-v6.es.net: Berkeley, CA
                                        </p>
                                        <p><em>Globus Service Access</em></p>
                                        <p>The test hosts are also available via the <a href="http://www.globus.org">Globus Transfer service</a>.  They are configured for anonymous, read-only access.</p>
                                        <p>anl-diskpt1.es.net is registered as the endpoint esnet#anl-diskpt1<br>
                                            bnl-diskpt1.es.net is registered as the endpoint esnet#bnl-diskpt1<br>
                                            lbl-diskpt1.es.net is registered as the endpoint esnet#lbl-diskpt1
                                        </p>
                                        <p><em>Sample GridFTP test commands</em></p>
                                        <p>If you don't have globus-url-copy installed, please refer to the GridFTP Quick Start Guide</p>
                                        <p>#make sure you can connect to server<br>
                                            globus-url-copy -list <a href="ftp://lbl-diskpt1.es.net:2811/data1/">ftp://lbl-diskpt1.es.net:2811/data1/</a><br>
                                            # copy 1G file<br>
                                            globus-url-copy -vb -fast <a href="ftp://lbl-diskpt1.es.net:2811/data1/10G.dat">ftp://lbl-diskpt1.es.net:2811/data1/10G.dat</a> file:///tmp/test.out<br>
                                            # copy 1G file using 4 parallel streams<br>
                                            globus-url-copy -vb -fast -p 4 <a href="ftp://lbl-diskpt1.es.net:2811/data1/10G.dat">ftp://lbl-diskpt1.es.net:2811/data1/10G.dat</a> file:///tmp/test.out<br>
                                            # write to /dev/null<br>
                                            globus-url-copy -vb -fast -p 4 <a href="ftp://lbl-diskpt1.es.net:2811/data1/10G.dat">ftp://lbl-diskpt1.es.net:2811/data1/10G.dat</a> file:///dev/null<br>
                                            # read from /dev/zero<br>
                                            globus-url-copy -vb -fast -p 4 -len 1G <a href="ftp://lbl-diskpt1.es.net:2811/dev/zero">ftp://lbl-diskpt1.es.net:2811/dev/zero</a> file:///tmp/t.out<br>
                                            # Use UDT instead of TCP<br>
                                            globus-url-copy -vb -udt <a href="ftp://lbl-diskpt1.es.net:2811/data1/10G.dat">ftp://lbl-diskpt1.es.net:2811/data1/10G.dat</a> file:///dev/null<br>
                                            Each host has a high-performance disk array, mounted as /data1. The following test files are available on each server, and are generated using "/dev/urandom" (the size is what you would expect from reading the filename):
                                        </p>
                                        <p>/data1/1M.dat, /data1/10M.dat, /data1/50M.dat, /data1/100M.dat,<br>
                                            /data1/1G.dat, /data1/10G.dat, /data1/50G.dat, /data1/100G.dat<br>
                                            In addition, there are currently several data sets composed of multiple files in a directory structure. These data sets are for testing multi-file transfers. The data sets each contain directories a through y. Each of these directories contains directories a through y. Each leaf directory contains data files named for their place in the directory structure. So, a-a-1M.dat is a 1,000,000 byte data file in the data set with path 5GB-in-small-files/a/a/a-a-1M.dat.  Note that the tiny file test set is primarily for testing directory creation performance, as the amount of data transferred will be trivial.
                                        </p>
                                        <p>The data sets are:</p>
                                        <p>/data1/5MB-in-tiny-files - 1KB, 2KB, and 5KB files in each leaf directory<br>
                                            /data1/5GB-in-small-files - 1MB, 2MB, and 5MB files in each leaf directory<br>
                                            /data1/50GB-in-medium-files - 10MB, 20MB, and 50MB files in each leaf directory<br>
                                            /data1/500GB-in-large-files - 100MB, 200MB, and 500MB files in each leaf directory<br>
                                            Sample commands for copying the complete data sets (these use the Berkeley DTN - substitute the other DTNs as needed):
                                        </p>
                                        <p># Copy using one stream only to test single-stream disk-to-disk performance<br>
                                            globus-url-copy -vb -p 1 -fast -r <a href="ftp://lbl-diskpt1.es.net:2811/data1/5GB-in-small-files/">ftp://lbl-diskpt1.es.net:2811/data1/5GB-in-small-files/</a> \<br>
                                            file:///some/path/5GB-in-small-files/<br>
                                            #<br>
                                            globus-url-copy -vb -p 1 -fast -r <a href="ftp://lbl-diskpt1.es.net:2811/data1/50GB-in-medium-files/">ftp://lbl-diskpt1.es.net:2811/data1/50GB-in-medium-files/</a> \<br>
                                            file:///some/path/50GB-in-medium-files/<br>
                                            #<br>
                                            # Copy using 4 parallel streams<br>
                                            globus-url-copy -vb -p 4 -fast -r <a href="ftp://lbl-diskpt1.es.net:2811/data1/5GB-in-small-files/">ftp://lbl-diskpt1.es.net:2811/data1/5GB-in-small-files/</a> \<br>
                                            file:///some/path/5GB-in-small-files/<br>
                                            #<br>
                                            globus-url-copy -vb -p 4 -fast -r <a href="ftp://lbl-diskpt1.es.net:2811/data1/50GB-in-medium-files/">ftp://lbl-diskpt1.es.net:2811/data1/50GB-in-medium-files/</a> \<br>
                                            file:///some/path/50GB-in-medium-files/<br>
                                            #<br>
                                            # Copy the big data set using 8 parallel streams<br>
                                            # (make sure your performance is good before doing this one!)<br>
                                            globus-url-copy -vb -p 8 -fast -r <a href="ftp://lbl-diskpt1.es.net:2811/data1/500GB-in-large-files/">ftp://lbl-diskpt1.es.net:2811/data1/500GB-in-large-files/</a> \<br>
                                            file:///some/path/500GB-in-large-files/
                                        </p>
                                        <p><a href="http://fasterdata.es.net/performance-testing/esnet-io-testers/">More information</a> about these hosts can be found on <a href="http://fasterdata.es.net/">ESnet's fasterdata site.</a></p>
                                    </div>
                                </div>
                            </div>
                            <div class="field field-name-field-file-attachments field-type-file field-label-above">
                                <div class="field-label">File Attachments:&nbsp;</div>
                                <div class="field-items">
                                    <div class="field-item even"><span class="file"><img class="file-icon" alt="PDF icon" title="application/pdf" src="/modules/file/icons/application-pdf.png"> <a href="https://icnwg.llnl.gov/sites/default/files/LLNL-HardwareRecommendationsforDTNnodes-150129.pdf" type="application/pdf; length=216390">LLNL-HardwareRecommendationsforDTNnodes-150129.pdf</a></span></div>
                                    <div class="field-item odd"><span class="file"><img class="file-icon" alt="PDF icon" title="application/pdf" src="/modules/file/icons/application-pdf.png"> <a href="https://icnwg.llnl.gov/sites/default/files/GlobusConnectServerInstall-llnl_0.pdf" type="application/pdf; length=88134">GlobusConnectServerInstall-llnl.pdf</a></span></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>