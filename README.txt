EXPIRY FILE BUILDER - Plant 1200 (Jeddah) / 2200 (Riyadh)
==========================================================

HOW TO OPEN
Double-click "Expiry File Builder.html" (Chrome or Edge), or open it with
VS Code Live Server. Keep the "lib" folder next to the HTML file.
No internet needed.

STEP 1 - SAP STOCK FILE
Upload 1200.xlsx or 2200.xlsx. The plant is detected automatically.
It stays loaded until you close or reload the page.

TAB: EXPIRY RETURN TXT
1. Upload a return / expiry Excel with columns:
   Material, Plant, Storage Location, Batch, Quantity, Supplier, Cost Price
2. Results: Available / Other batch / Other location / Not enough / Data error
3. Click Generate. The TXT gets the same name as the Excel file.
4. Exported quantities are deducted; the next Excel is checked against what is left.

TAB: OVERSTOCK TRANSFER
Lists all stock in x204 and x208 (1204/1208 or 2204/2208) and asks to approve.
   Material 1xxxxx -> 1100 / 1110   (2100 / 2110)   group INM   Doc 1
   Material 2xxxxx -> 1100 / 1120   (2100 / 2120)   group INC   Doc 2
   Material 3xxxxx -> 1100 / 1130   (2100 / 2130)   group INC   Doc 3
   Material 4xxxxx -> 1100 / 1140   (2100 / 2140)   group INC   Doc 4
BATCH RULES
   Medicine (1xxxxx) moves ONLY with a real batch - DUMMY batch is kept out.
   Materials 2, 3, 4 move ONLY with batch DUMMY - other batches are kept out.
Kept-out lines are saved in a separate Excel:
   "OS 1200 dd-mm-yyyy - Batch exceptions.xlsx"
   sheet "Medicine DUMMY batch" and sheet "Batch not DUMMY"
Click "Approve transfer", then "Approve and download".
The file is saved as "OS 1200 dd-mm-yyyy.xlsx" (or OS 2200 ...) in the
MED OS upload format. Transferred quantities are removed from session stock.

NOTES
- Use "Undo deduction" in the Session log if you exported by mistake.
- Stock and deductions reset when you close or reload the page.
