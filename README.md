# PDF_OVERLAY
System to overlay text on a PDF file based on inputs from Excel sheets

Test Process:\
(1) Run the main.py file, and follow the instructions.\
(2) The system needs a PDF file and a TEMPLATE.xlsx file to operate.\
(3) The system will create multiple numbers of PDF files as output based on the instructions in the TEMPLATE.xlsx

Test Passwords:\
(1) EMP01 - perdata\
(2) PAY01 - saldata\
(3) TEMPLATE - NO PASSWORD


# User Manual

This tool creates a text overlay on any PDF file based on the input given in the TEMPLATE.xlsx. PDF_OVERLAY supports two types of content:\
(1) Immediate text **<Type=Text>**\
(2) Text extracted from a data file **<Type=File>**
The system will search the file for a primary key and will get a value from the matching row as the text. The list of primary keys are listed in the **data** tab of the TEMPLATE.xlsx.\

Once processed, the output file name will be created by combining the text in **Primary Key**\
column and **Identifier** column in the **data** tab.

The Required Information to generate a new PDF_OVERLAY File:\
(1) **Date** \
(2) **Year of Assessment**\
(3) **Employers' TIN** \
(4) **Employees Full Name** \
(5) **NIC Number**\
(6) **Birth Day**\
(7) **Date of Join**\
(8) **Basic Salary**

When it extracts data from a file, It considers these arguments:\
(1) **File**-  Name of the related .xlsx file.\
(2) **Sheet**-  The relevant sheet name.\
(3) **PrimeryKey**-  The primery key column name.\
(4) **Value**-  The column name for the value we want.

PDF_OVERLAY supports six types of params:\
(1) **X** (compulsory) can be given in pixels (875), inches (2.34in), or millimeters (34mm)\
(2) **Y** (compulsory) can be given in pixels (875), inches (2.34in), or millimeters (34mm)\
(3) **Font** (optional, if not specified will be set to default = "Helvetica")\
(4) **FontSize** (optional, if not specified will be set to default = 12)\
(5) **LineSpace** (optional, if not specified will be set to default = 1.2X)\
(6) **Function** (optional, if not specified will be set to default = None)

Param Functions are executed when overlaying the content. Supported functions are below.\
(1) **SrinkToFit(width ,maxLines)**

PDF_OVERLAY supports three types of text preprocessors:\
(1) **AddSpace(text,spaceCount)**\
(2) **NumberToText(text,Type) Type can be "Integer" or "Float"**\
(3) **NumberToCurrency(text,currency,numberofDecPoints)**
