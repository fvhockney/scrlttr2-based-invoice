# scrlttr2-based-invoice
Invoice and Letter Combo based on scrlttr2 Latex

This is an initial working example of a letter/invoice combo I am using.

I have broken this down into several smaller files which are included in the main tex file to be used when compiling.

Items in the `_globalVariables` file should not need to be changed after personalizing them.

Items which may need to be changed for each letter/invoice are located in `_userVariables`. By only having one file that needs to be updated regularly mitigates the amount of time needed to find the various components when making an invoice. It also mitigates the possibility of causing the file to break accidentally.

Known Issues (To Be Fixed):

Formatting error in `\entries` located withing longtable in `_userVariables`

`\vat` must be set in `_globalVariables` right now...that should be moved to `_userVariables`

`\vat` must be entered as a decimal. This means we have to set it as a non-decimal in longtable in `_userVariables`. It would be better if `\vat` were set as a non-decimal and automatically calculated to a decimal to be used in calculations.

Still need to add better header and footer support for additional information such as e-mail and phone number.

`plengths` have to be adjusted manually for the invoice page if the letter head expands. These need to be set dynamically.
