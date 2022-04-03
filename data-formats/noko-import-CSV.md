# Creating a Noko import CSV file

Do you have  **historical time tracking data**  you want to import into Noko? Perhaps you have an  **internal tool**  and occasionally need to move entries into Noko? Whatever the reason, here's how you **create a**  **CSV file for importing your data**.

Noko can also automatically convert and understand CSV files from other time tracking apps, namely  **Harvest, Basecamp, Freshbooks, Tempo, Toggl** and **Tick**. If you have a CSV export from on of these apps, please read our article on  [importing time tracking data from other apps](https://help.nokotime.com/article/32-importing-time-tracking-data-from-other-apps).

#### Noko CSV format fields

| **Field name** | **Type** |  **Example** | **Required** | **Description** |
| --- | --- | --- | --- | --- |
| date | Date | 2015-08-09 | required | Date the entry is logged for. _While Noko automatically detects and understands various date formats, we recommend using ISO dates (YYYY-MM-DD)._ |
| person | String | "Thomas Fuchs" | optional* | The name of the person the entry is for. This tries to match the name given with a person in your Noko account. If you also give an email address, we try to match the email address first. You must supply either the person or the email field (or both). |
| email | String | thomas@slash7.com | optional* | The email of the person the entry is for. Giving an email adress takes precedence over the person field. You must supply either the person or the email field (or both). |
| group/client | String | "Slash7 LLC" | optional | If the project given doesn't exist yet, and the option to automatically create projects is turned on for the import, this project group name will be set for the new project. If multiple different project group names are given throughout the import file, the first one found will be used.  The project group name will be ignored if the project already exists in Noko.  Project group names can be up to 255 unicode characters in length. |
| project | String | "Noko" | optional | The project the entry is assigned to. If the project given doesn't exist yet, and the option to automatically create projects is turned on for the import, this project will be automatically created. Project names can be up to 100 unicode characters in length. |
| minutes | Number | 120 | optional* | The amount of time the entry is for in minutes.  _If both the minutes and hours field is given, minutes takes precedence and the hours field is ignored. If neither minutes or hours is given, the entry will be set to 0 (zero) minutes._ |
| hours | Number/Time | 4 or 4:30 | optional* | The amount of time the entry is for in hours. The hours field can either a number (4 for four hours, 4.5 for 4 hours, 30 minutes, etc) or a time given as hours:minutes. _If both the minutes and hours field is given, minutes takes precedence and the hours field is ignored. If neither minutes or hours is given, the entry will be set to 0 (zero) minutes._ |
| tags | String | "#importing, #data" | optional | The tags used in this entry. If no description field is given, the description for the entry will be made up of the tags in the tags field in the given order. Noko will automatically create new tags if the tags given in the entry don't exist in Noko. If a description is given, the tags field will be ignored. |
| description | String | "Trying out #importing some #data" | required | The description for the entry. If this field is given, the tags field will be ignored. Noko will automatically create new tags if the tags given in the description don't exist in Noko. |
| billable | String | yes/no | optional | Whether or not the entry is billable. Defaults to yes. |

Noko CSV files should be in  **Unicode (UTF-8)**  format, with  **commas (",") as delimiters**  and  **quoted strings**  when necessary.

To  **export a CSV file from Excel**, simply do  **Save as…**  and select  **Comma Separated Values (.csv)**  as the file format:

Here's a simple example of a  **CSV file with a few entries**:

```
date,email,project,minutes,description
8/9/15,thomas@slash7.com,Noko,120,Trying out #importing some #data
8/7/15,unknown@email.com,Internal,60,"Getting down to #inbox zero, setting up some #email rules"
8/6/15,devon@slash7.com,Internal,30,Creating #chaos
```
