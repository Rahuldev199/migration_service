<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
    <title>Daily Report</title>
</head>

<body style="color: #000000; font-family: Arial, sans-serif; background: #E9EAEC; padding-left: 25px; min-width: 95%;">
    <table>
        <tr>
              <td>
                <table >
                    <tr>
                          <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">
                            <div style="font-weight: 200;font-size: 14pt;padding-bottom: 5px;padding-top: 25px;text-transform: uppercase;">
							 ORDER COUNT
                            </div>
                            <div>
                                 <table style="background-color: whitesmoke;  border: 1px solid #000000;  margin: 5px 0;  font-size: 0.9em;  font-family: sans-serif;  min-width: 95%;  table-layout: auto;  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);">
                                   <tr style="background-color: #333652;color: #ffffff !important;text-align: left;text-transform: uppercase;">
                                        <th>Flow Types</th>
                                        <th>ORDER COUNT</th>
                                    </tr>
                                    <#list ordercount as item>
                                        <tr>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${(item.flowtype)!"-"}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${(item.ordercount)!"-"}</td>
                                        </tr>
                                        <#else>
                                            <tr>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>

                                            </tr>
                                    </#list>
                                </table>
                            </div>
                            <div style="font-weight: 200;font-size: 14pt;padding-bottom: 5px;padding-top: 25px;text-transform: uppercase;">
                                SUMMARY
                            </div>
                            <div>
                                 <table style="background-color: whitesmoke;  border: 1px solid #000000;  margin: 5px 0;  font-size: 0.9em;  font-family: sans-serif;  min-width: 95%;  table-layout: auto;  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);">
                                    <tr style="background-color: #333652;color: #ffffff !important;text-align: center;text-transform: uppercase;">
                                        <th colspan="1"></th>
                                        <th colspan="3">DataSync</th>
                                        <th colspan="2">DataCompare</th>
                                        <th colspan="2">Payload</th>
                                    </tr>
                                    <tr style="background-color: #333652;color: #ffffff !important;text-align: center;text-transform: uppercase;">
                                        <th>Flow Type</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                        <th>INPROGRESS</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                    </tr>
                                    <#list summary as item>
                                        <tr>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datasync_type?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datasync_success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datasync_failure?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datasync_inprocessing?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datacompare_success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.datacompare_failure?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.apicompare_success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.apicompare_failure?if_exists}</td>
                                        </tr>
                                        <#else>
                                            <tr>
                                            	  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                            </tr>
                                    </#list>
                                </table>
                            
                            <div style="font-weight: 200;font-size: 14pt;padding-bottom: 5px;padding-top: 25px;text-transform: uppercase;">
                                DATA COMPARE
                            </div>
                            <div>
                                 <table style="background-color: whitesmoke;  border: 1px solid #000000;  margin: 5px 0;  font-size: 0.9em;  font-family: sans-serif;  min-width: 95%;  table-layout: auto;  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);">
                                   <tr style="background-color: #333652;color: #ffffff !important;text-align: left;text-transform: uppercase;">
                                        <th>Flow Types</th>
                                        <th>MILESTONE</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                    </tr>
                                    <#list datacompare as item>
                                        <tr>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.flowtype?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.milestones?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.failure?if_exists}</td>
                                        </tr>
                                        <#else>
                                            <tr>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>

                                            </tr>
                                    </#list>
                                </table>
                            </div>
                            <div style="font-weight: 200;font-size: 14pt;padding-bottom: 5px;padding-top: 25px;text-transform: uppercase;">
                                API COMPARE
                            </div>
                            <div>
                                 <table style="background-color: whitesmoke;  border: 1px solid #000000;  margin: 5px 0;  font-size: 0.9em;  font-family: sans-serif;  min-width: 95%;  table-layout: auto;  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);">
                                   <tr style="background-color: #333652;color: #ffffff !important;text-align: left;text-transform: uppercase;">
                                        <th>Flow Types</th>
                                        <th>API TYPE</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                    </tr>
                                    <#list apiCompare as item>
                                        <tr>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.flowType?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.apiType?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.failure?if_exists}</td>
                                        </tr>
                                        <#else>
                                            <tr>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                            </tr>
                                    </#list>
                                </table>
                            </div>
                            
                            <div style="font-weight: 200;font-size: 14pt;padding-bottom: 5px;padding-top: 25px;text-transform: uppercase;">
                                DATA SYNC
                            </div>
                            <div>
                                 <table style="background-color: whitesmoke;  border: 1px solid #000000;  margin: 5px 0;  font-size: 0.9em;  font-family: sans-serif;  min-width: 95%;  table-layout: auto;  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);">
                                   <tr style="background-color: #333652;color: #ffffff !important;text-align: left;text-transform: uppercase;">
                                        <th>Flow Types</th>
                                        <th>TYPE_DEF_NAME</th>
                                        <th>SUCCESS</th>
                                        <th>FAILURE</th>
                                        <th>INPROCESSING</th>
                                    </tr>
                                    <#list datasync as item>
                                        <tr>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.flowType?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.typedefname?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.success?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.failure?if_exists}</td>
                                              <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">${item.inProgress?if_exists}</td>
                                        </tr>
                                        <#else>
                                            <tr>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                                  <td style="border: 1px solid #000000;padding: 5px 5px 5px 5px;">0</td>
                                            </tr>
                                    </#list>
                                </table>
                            </div>
                        </td>
                    </tr>
                </table>
            </td>
        </tr>
    </table>
</body>

</html>
