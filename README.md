# Amazon QuickSight Workshop Guide

Amazon QuickSight is AWS's cloud-native, serverless business intelligence (BI) service that enables you to create and publish interactive dashboards with data visualizations, ML-powered insights, and natural language queries.

---

## Part 1: Create Analysis in QuickSight

### Step 1 – Create Your Dataset

1. From QuickSight console's left pane, choose **Datasets**
2. In the upper right of your screen, click **New dataset** button
3. Choose the first option called **Upload a file**
4. Download the sample data: [SaaS-Sales.csv](SaaS-Sales.csv)
5. Upload the file and choose **Next**
6. Choose **Visualize**

You are now in an Analysis view. This is where you can add visuals, adjust the layout and then publish your dashboard.

7. On the **New sheet** pop-up, leave **Interactive sheet** selected and click the **CREATE** button
8. Take a moment to familiarize yourself with the page elements

---

### Step 2 – Visualize Sales by Month

1. Click the empty visual to ensure that it is selected (indicated by black border)
2. From the **Fields list** in primary left pane, select **Sales** and **Order Date**
3. Enlarge the visual if axis labels are not visible
4. Click the arrow next to the **Order Date** label on your X-axis and choose **Aggregate → Month**

**Alternative method:**
- Click the ellipsis against **Order Date** field from secondary left pane → **X AXIS** section to access the visual-level field menu

---

### Step 3 – Add Forecast to Line Chart

Let's use the in-built forecasting feature to add a forecast to our line chart.

1. From the visual menu in the upper right of the visual, click the **ellipsis icon**, and choose **Add forecast**

**Optional - Backward Forecast:**
2. When adding/editing the forecast, you can apply backward forecast to see how close the forecast is to the actuals for previous months
3. Change **Periods backward** to `6`, scroll down in right pane, click **Apply** and check out the backward forecast
4. Then, change **Periods backward** back to `0` and click **Apply**
5. Close the **Forecast properties** right pane

---

### Step 4 – Visualize Sales Quarter over Quarter

1. From top toolbar, click the **Add visual** (line-chart) icon and select **Key Performance Indicator (KPI)**
   - **Alternative:** Access the visual type selector from secondary left pane by clicking the dropdown on **+ADD** button

2. From **Fields list**, select **Sales** and **Order Date**

3. Open visual-level field menu for **Order Date** and change the aggregation to **Quarter**
   - **Hint:** Secondary left pane → **TREND GROUP** → Ellipsis against Order Date field

4. **Optional:** Click **KPI LAYOUTS** from secondary left pane and try clicking the layout options presented. Finally, select the **Vertical layout with primary actual value (first)** option and click **<** to return to Visuals view
   - If you accidentally closed the secondary left pane, reopen it by clicking **visualize** (bar-chart) icon from top toolbar

5. In the right pane **Properties** view, expand **KPI options** section and change:
   - **Primary value displayed** to **Comparison**
   - **Comparison method** to **Difference**

6. Further down in right pane, click the **Tooltip** toggle to enable it
   - This will let you see data for prior quarters by hovering over the sparkline

7. Resize the visual and move it to the right of the line chart

---

### Step 5 – Add Suggested Insights

1. With the KPI visual selected, click the **Insights** (bulb) icon from top toolbar
   - This opens **Suggested insights** in secondary left pane

2. Click the **+** button on the **MONTH OVER MONTH CHANGE** suggested insight to add it to the canvas

3. Repeat step 1 to open the **Suggested insights** pane again

4. Click the **+** button on the **FORECAST** suggested insight to add it to the canvas

5. Resize the insights to be smaller, and move them to the right, just beneath your KPI visual

---

### Step 6 – Visualize Sales by Industry

1. From top toolbar, click the **Add visual** (line-chart) icon and select **Donut chart**

2. From **Fields list**, select **Industry** and **Sales**

3. Expand the **Data labels** section in right pane
   - **Note:** Properties view should already be open in right pane. If you closed it, click the **Properties** (Pencil & chart) icon from top toolbar or the **Format visual** (pencil) icon in visual menu to open it again

4. Click the **eye-slash** icon against **Metric** to show measure values

---

## Part 2: Create Q Topic in QuickSight

Amazon Q enables natural language queries on your data.

---

### Step 1 – Create a Dataset

**If you already have SaaS-Sales dataset from Part 1, skip to Step 2.**

1. Download [SaaS-Sales.csv](SaaS-Sales.csv)
2. In QuickSight, from **Datasets** view, click **New dataset** button
3. Select **Upload a file** option and choose the **SaaS-Sales.csv** file from local
4. Click **Edit settings and prepare data** button
5. Click **SAVE & PUBLISH** button
6. Click **QuickSight** icon to exit dataset edit screen

---

### Step 2 – Create a Topic

1. From **Topics** view, click the **NEW TOPIC** button

2. Enter the following details:
   - **Name:** `SaaS-Sales-<your-name>`
   - **Description:** `Use this topic to ask questions regarding software sales`
   - Click **Continue** button
   - *Note: Your topic users will see this description*

3. In **Select a dataset** pop-up, choose **SaaS-Sales** from dataset list and click **Continue** button

4. Wait for Q to index the data and set up field configurations
   - This can take a few minutes
   - The status column shows the progress of this task

---

### Step 3 – Explore Q Panel

1. Open the newly created topic (**SaaS-Sales**) and click the **Ask a question about SaaS-Sales** button from top menubar
   - This opens up the Q panel to SaaS-Sales

2. Type into Q search bar: `Show me total sal`
   - Note that Q provides type-ahead assistance using both field names and field values
   - Select **Sales** from the options presented and hit enter/return or click **ASK** button

3. Explore **Suggested Questions**
   - These are prepopulated with AI-generated options
   - Once you add verified questions later on, they will show up here as well
   - Try clicking a few suggested questions

4. Ask Q: `show me monthly sales for ContactMatcher`
   - Note that Q provides a restatement of how it interpreted your question: *"Total Sales by month for Product ContactMatcher"*

5. Click on **pencil icon** to open restatement edit mode
   - Note that Q provides options to modify the restatement if needed
   - Edit mode also shows which dataset is being used to answer the question

---

### Step 4 – Add Dataset to Topic

*(Content appears to be incomplete in the original. Add additional steps as needed)*

---

## Resources

- **Sample Data:** SaaS-Sales.csv
- **AWS QuickSight Documentation:** https://docs.aws.amazon.com/quicksight/
- **QuickSight Community:** https://community.amazonquicksight.com/

---

## Key Features Demonstrated

✅ **Data Visualization** - Line charts, KPI visuals, donut charts  
✅ **ML Insights** - Forecasting, suggested insights  
✅ **Natural Language Queries** - Amazon Q for plain English questions  
✅ **Interactive Dashboards** - Filters, drill-downs, tooltips  
✅ **Data Analysis** - Aggregations, time-series analysis, comparisons

---

## Next Steps

- Publish your analysis as a dashboard
- Share with team members
- Set up scheduled email reports
- Explore additional visual types
- Create custom calculated fields
- Set up row-level security

---

## Troubleshooting

**Issue:** Visual not displaying correctly  
**Solution:** Ensure fields are properly selected and aggregated

**Issue:** Q not understanding questions  
**Solution:** Use field names from your dataset, add synonyms in topic settings

**Issue:** Forecast not appearing  
**Solution:** Ensure you have sufficient historical data (at least 15 data points recommended)

---

## Support

For questions or issues, refer to:
- AWS QuickSight Documentation
- AWS Support Console
- QuickSight Community Forums
