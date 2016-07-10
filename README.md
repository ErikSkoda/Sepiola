# Sepiola
Sepiola test automation tool

Summary
Tool for quickly and easily creating data driven testscripts and testdata regardless of which technolgy you are using. However it's use is not limited to testing. You could just as well create mailings.

Why use Sepiola?
In test automation, especially in Agile, there is a constantly reoccurring need for generating and maintaining large quantities of testscripts and testdata. To get test coverage, you will usually need variations of the same scripts or files while only tweaking a few parameters. Doing this manually is tedious, time consuming, error prone and if you make a mistake it will cost you more time. With Sepiola you can automate the task.

What can I use Sepiola for?
For generating XML files for soapUI mockervices or Selenium, FitNesse or Java scripts. You can also use it for generating a number of similar SQL queries for a CRUD test or for creating batch files or shell scripts.

What does Sepiola do?
Sepiola merges data in Excel with a template text file.

Does Sepiola also perform checks on WSDL's and XSD's?
No. It just merges data with a template.

Can I also use it to create EDIFACT files?
Of course. Sepiola knows nothing about soapUI, XML, SOAP, Java or Edifact. All it does is merging data and a template. Because it is not linked to any one technology you can apply it to all. If you want to create EDIFACT files, or Perl, Grease Monley, JSON or any other kind of script or data file, you can do so.

How long will it take to learn?
A couple of minutes using an example as a starting point.

What other tools do I need to generate data driven files with Sepiola?
Microsodt Excel and a text editor.

How do I install Sepiola?
Copy the Sepiola Excelsheet (Sepiola.xlsm) into a folder.

How do I run Sepiola?
Run the macro Sepiola. 

How do I activate macros in Excel?
Google: "enable excel macro" and you will find a number of youtube clips lasting about 90 seconds showing you how to do it for various versions of Microsoft Excel.

In the 2013 version (I'm using a Dutch version, my translation of the commands may not be 100% identical to what you see) do the following:
open Excel
click the Office button at the top left of your Excel window
in the menu click the button "Excel Options" (botton left)
click on "Trust Center" (left panel)
click the button "Trust Center settings" (bottom right)
The radio button "Enable all macro's" (right panel) is the one I have activated.
I have also checked the checkbox "Trust access to the VBA object model"
Click "OK"".
Reopen Excel options (Office Button, Excel options)
Click "Customize" in the left panel (6th from top, the one below "Advanced")
double click on "Show macros" in the left list. It will now show up on the right.
Click "OK".

How do I see if Sepiola is working?
Check the folder where you installed Sepiola. After running the Sepiola macro, you should see the logfile: sepiola.xlsm.log.

How do I declare parameters in Sepiola?
By adding them in the first row of the data sheet (worksheet: "Iterative data")

How do I add data to those parameters?
By adding data in the columns below the parameters in the data sheet.

How do I add a template to Sepiola?
Create a text file in the same folder where you have Sepiola installed. Rename it to: sepiola.xlsm_body.txt.

How do I add parameters to my template?
If you have declared a parameter ZipCode in your data sheet, Sepiola will look for the tag <ZipCode#> in the template to replace it with your data. Just add <ZipCode#> to your template where you want to use it.

Where can I find the data driven scripts or date generated by Sepiola?
In the same folder where you have installed Sepiola.

Will I get the results in one file or will I get one file for each variation in parameters?
You will get both. You can use whichever is most practical for you. If you have 3 rows of data, you will get the files sepiola_1.txt, sepiola_2.txt, sepiola_3.txt as well as sepiola_batch.txt.

Is there an easier way to add parameters to my template?
Yes. In Sepiola.xlsm, go to the worksheet "SupportInfo". Look for the cell saying: "Iterative tagnames available for use in body template. Copy and Paste from here to avoid typos." Below you will find a list of tags based on your parameter names.

Can I change the names of the output files?
To customize the output filenames, open your data sheet and add the parameter [FileName] (case sensitive). Fill in the desired output filename. You don't need to use it in your template.

Can I change the name of the Excelsheet containing Sepiola?
Just as long as you don't change the extension .xlsm. Also, you need to rename the template accordingly. When you rename sepiola.xlsm to mock.xlsm, Sepiola will be looking for a template named mock.xlsm_body.txt.

Anything I should avoid?
Deleting or inserting rows or columns in the data sheet will mess up your support info sheet from where you can copy and paste parameters into your template.

Can I use Excel functionality like conditional formatting to check for double values and still run Sepiola?
Of course.

Do I need to change any registry settings or set environment variables to Run Sepiola?
No.

Any other requirements?
You need to have write access in the folder where you have Sepiola installed.
