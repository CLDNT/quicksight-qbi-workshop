# quicksight-qbi-workshop

**Part-1: Create Analysis in QuickSight**

**Step 1 – Create your dataset**
From QuickSight console's left pane, choose Datasets.
In the upper right of your screen, click New dataset button.
Choose the first option called Upload a file.
In the repo Download: SaaS-Sales.csv
Choose Next.
Choose Visualize.
You are now in an Analysis view. This is where you can add visuals, adjust the layout and then publish your dashboard. First, let's add a sheet, set the display mode and change the name of this analysis.

On the New sheet pop-up, leave Interactive sheet selected and click the CREATE button.
Please take a moment to familiarize yourself with the page element names marked below.

**Step 2 – Visualize Sales by Month**
Click the empty visual to ensure that it is selected (indicated by black border).
From the Fields list in primary left pane, select Sales and Order Date.
Enlarge the visual if axis labels are not visible.
Click the arrow next to the Order Date label on your X-axis and choose the Aggregate->Month.
Alternatively, you can click the ellipsis against Order Date field from secondary left pane > X AXIS section to access the visual-level field menu to make this aggregate change.

**Step 3 – Add Forecast to Line Chart**
Let's use the in-built forecasting feature to add a forecast to our line chart.

From the visual menu in the upper right of the visual, click the ellipsis icon, and choose Add forecast.
Optional - when adding/editing the forecast, you can apply backward forecast as well to see how close the forecast is to the actuals for the previous months.
Change Periods backward to 6, scroll down in right pane, click Apply and check out the backward forecast.
Then, change Periods backward back to 0 and click Apply.
Close the Forecast properties right pane.

**Step 4 – Visualize Sales Quarter over Quarter**

From top toolbar, click the Add visual (line-chart) icon and select Key Performance Indicator (KPI).
Alternatively, you can access the visual type selector from secondary left pane by clicking the dropdown on +ADD button.
From Fields list, select Sales and Order Date.
Open visual-level field menu for Order Date and change the aggregation to Quarter.
Hint - Secondary left pane > TREND GROUP > Ellipsis against Order Date field.
Optional - Click KPI LAYOUTS from secondary left pane and try clicking the layout options presented in KPI Layouts pane. Finally, select the Vertical layout with primary actual value (first) option and click the < to return to Visuals view.
If you accidentally closed the secondary left pane, you can reopen it by clicking visualize (bar-chart) icon from top toolbar
In the right pane Properties view, expand KPI options section and change Primary value displayed to Comparison.
Change Comparison method to Difference.
Further down in right pane, click the Tooltip toggle to enable it.
This will let you see data for prior quarters by hovering over the sparkline. Try it by hovering over the area sparkline in the KPI visual.
Resize the visual and move it to the right of the line chart.

**Step 5 – Add Suggested Insights**

With the KPI visual selected, click the Insights (bulb) icon from top toolbar.
This opens Suggested insights in secondary left pane.
Click the + button on the MONTH OVER MONTH CHANGE suggested insight to add it to the canvas.
Repeat step 1 to open the Suggested insights pane again.
Click the + button on the FORECAST suggested insight to add it to the canvas.
Resize the insights to be smaller, and move them to the right, just beneath your KPI visual.

**-------------------------------------------------------------------------------**
**Part-2: Create Q Topic in QuickSight**


**Step 1 - Create a dataset**
If you already have SaaS-Sales dataset (from Previous Step workshop), skip to Step 2.
Download **SaaS-Sales.csv**
In QuickSight, from Datasets view, click New dataset button.
Select Upload a file option and choose the SaaS-Sales.csv file from local.
Click Edit settings and prepare data button.
Click SAVE & PUBLISH button.
Click QuickSight icon to exit dataset edit screen.

**Step 2 - Create a topic**
From Topics view, click the NEW TOPIC button.
Enter name as **SaaS-Sales-<your-name>**, Paste in the description - Use this topic to ask questions regarding software sales and click Continue button.
Your topic users will see this description.
In Select a dataset pop up, choose SaaS-Sales from dataset list and click Continue button.
Q needs to index the data and set up field configurations as part of topic creations. This can take few minutes. The status column shows the progress of this task.

**Step 3 - Explore Q Panel**
Open the newly created topic (SaaS-Sales) and click the Ask a question about SaaS-Sales button from top menubar.
This opens up the Q panel to SaaS-Sales.
Type into Q search bar : Show me total sal
Note that Q provides you type ahead assistance and uses both field names and field values for this.
Select Sales from the options presented and hit enter/return or click ASK button.

Suggested Questions is prepopulated with AI generated option.
Once we add verified questions later on, they will show up here as well.
Try clicking few suggested questions.

Ask Q - "show me monthly sales for ContactMatcher"
Note that Q provides a restatement of how it interpreted your question.
"Total Sales by month for Product ContactMatcher."
Click on pencil icon to open restatement edit mode.
Note that Q gives provides option to modify the restatement if needed.
Edit mode also shows which data set is being used to answer the question.

**Step 4 - Add Dataset to Topic**
