# Importing a Part List from Excel
Otimize Nesting is a productivity software tool, first and foremost. It includes the features you need for highly productive part nesting creation.

If there is a feature that is common to all productivity applications, it is the ability to read data from Excel spreadsheets. The spreadsheets are usually manually created for example in Microsoft Excel or automatically created by another software program.

This topic covers the basics of importing rectangular part lists and helps you save time.

> [!NOTE]
> Special CAD or ERP systems can also create digital files with part lists to improve system integration. These files can be also imported in Otimize Nesting


There are two main steps to bringing your existing part list to Otimize Nesting. The first step is to prepare the a file, and the second part is to import the file into Otimize Nesting.

## Part 1: Prepare the Part List File
Prepare a spreadsheet containing the list of parts you want to produce. Otimize Nesting expects a given spreadsheet column position for each part information. The following image shows a sample part list.

![Example Part List](./import-excel/importExcelPartList.png)

When all the data is added to the spreadsheet, please save it to a file on your local computer.

You must save this file in CSV (Comma Separated Values) format, a text file containing your entered values, separated by a unique character.

1.	Go to your spreadsheet in Microsoft Excel and select **File** -> **Save As**.
2.	A dialog is shown. Select the desired folder, enter the file name, and make sure to select **CSV (Comma delimited) (*.csv)** save as type.

Alternatively, [download this sample .csv file](./import-excel/SampleCSVPartList.csv) with the correct column formatting and use it as a model for your part lists.

## Part 2: Import the Part List File

1.	Start Otimize Nesting.
2.	Create a new or open an existing project. Go to the **Parts** tab.
3.	Select **Import Parts** -> **csv**.

![Import Parts](./import-excel/importExcelImportCSV.png)

4.	The **Open** file dialog is displayed. Find and select the .csv file you saved before. Select **Open**.
5.	The **Import File** page is displayed with the part list.

![Import Page](./import-excel/importExcelImportPage.png)

6.	Select **Import**. The parts will be added to the project, and the Part tab will be displayed again.

![Imported Parts](./import-excel/importExcelImportedParts.png)

## Troubleshooting

### Regional Settings

Different languages and regions may use different column separation characters for spreadsheets. If you experience errors in the **Import File** page:
1.	Select the correct separator
2.	Select **Refresh** to have the data updated

![Select Separator](./import-excel/importExcelIncorrectSeparator.png)

### Row Headers

Typically, spreadsheets contain header column names on the first row. This or any other row can be ignored on the **Import File** page.

![Ignore Rows](./import-excel/importExcelIgnoreRows.png)
