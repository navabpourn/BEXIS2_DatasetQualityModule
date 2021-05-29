# BEXIS2_DatasetQualityModule
This is a module for visualizing the dataset quality for BEXIS2.
To use this module you need to 
1) Add the following code into the ~\Core\Console\BExIS.Web.Shell\Areas\DDM\Views\Data\ShowData.cshtml in the right place. 
    show_tabs.Add("show_dq_tab", "true");
2) Add the following code into the same file in the right place.
    tabs.Add()
        .Text("Dataset Quality")
        .LoadContentFrom("ShowDQ", "DQ", new { area = "dqm", datasetID = @Model.Id, versionId = Model.VersionId })
        .HtmlAttributes(new { id = "dq" })
        .Enabled(true);
3) Create the following files in ~\Data\DatasetQualities.
    Comparison.csv
    datasetInfo.csv
    PerformerDataset.csv
    Performers.csv
    Variables.csv
4) Add the module files in ~\Core\Console\BExIS.Web.Shell\Areas\DQM.
