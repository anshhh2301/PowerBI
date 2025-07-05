# FurniturePro Dashboard

### Dashboard Link : https://drive.google.com/file/d/1PycQvPzgxgQWO26IBall36VgBZJnmqkF/view?usp=sharing


## Problem Statement

This dashboard helps the FurniturePro understand their sales, profit and customers better. It helps them to understand their overall/monthly revenue, top customers and details about their products. Through different KPIs and visuals, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know which product or which customer are giving us more/less sales and hence improving ny identifying the problem. This report contains many analysis techniques like Pareto Analysis, RFM Analysis and Profit Analysis that helps us understand the insights and contributing factors to the sales.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in some of the columns there were some errors.
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Since we have many pages in the report, one page was created for the Overview of the store, the other was for Country wise sales details, then Product details, Customer details and some AI insights were added for further reference.
- Step 7 : Many DAX measures were created for the visuals to be dynamic and also to get some deeper insights into the data.
- Step 8 : Visual filters (Slicers) were added for the user to filter the visuals according to their choice.

  

Some of the DAX expressions and their visuals are represented below:

1. Total Revenue
       
      Total Sales = SUM(Orders[Sales Amount])
        

![Total Revenue](https://private-user-images.githubusercontent.com/219225965/462771429-69f5fa34-aca6-47c6-a054-a2a4fdbf0a65.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjAyNTEsIm5iZiI6MTc1MTcxOTk1MSwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNDI5LTY5ZjVmYTM0LWFjYTYtNDdjNi1hMDU0LWEyYTRmZGJmMGE2NS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjUyMzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZTg3MjMwMzBhN2VkNjQ4YmJkZWE3ZDBlMjA0ODZiMTE3YjZjN2IyNjIwMWQ0NDY5MzAyNGU0ZDQxOGNkM2FjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.DXJTrnEvTmt5TyMNWgz6KlnFh4eToMEkbMgdooGp1iw)
        
2. Total Profit

        Total Profit = SUM(Orders[Profit])

![Return_Rate](https://private-user-images.githubusercontent.com/219225965/462771542-2b7a0ae3-1e20-473b-a8dd-8585a23d2c6f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjAzMDcsIm5iZiI6MTc1MTcyMDAwNywicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNTQyLTJiN2EwYWUzLTFlMjAtNDczYi1hOGRkLTg1ODVhMjNkMmM2Zi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjUzMjdaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03YmM2YWJmNTBhM2U1Njg3MjYyMzdhMjUwMTFkZTdhOWYwYzliZWQ2ZWFjNDgyZjM5MDhhMTM4YmE3MDk2OTYzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.gzbVEy0n_jiWkg_WZqqpVPuOixgv65S3EuOe1evm75g)

        
3. Total Quantity

        Total Quantity = SUM(Orders[Quantity])
 
 ![Snap_3](https://private-user-images.githubusercontent.com/219225965/462771589-9f5944fb-00a7-443e-8b02-6e28eb62bcfd.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjAzNTUsIm5iZiI6MTc1MTcyMDA1NSwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNTg5LTlmNTk0NGZiLTAwYTctNDQzZS04YjAyLTZlMjhlYjYyYmNmZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjU0MTVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kY2IyZDUxMzFhNTU1OWIzZjRmNDYyYjU5YzUxYTUwNWM1MjkzZmFmYmFmZjcyMDAwNWNiMTNmZjcyZTc1MDIxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.PSiMSXCT95m-ZvXLk6VeWVJyWaO5XcIoh9gs3x4i-u8)

 
4. Average Recency

 
       RFM table = SUMMARIZE(
   'Orders','Orders'[Customer ID],
   "R Value",[R Value],
   "F Value",[F Value],
   "M Value",[M Value])

 ![Snap_4](https://private-user-images.githubusercontent.com/219225965/462771622-274c2725-0043-4be1-8c77-b95a5130efe7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjAzODcsIm5iZiI6MTc1MTcyMDA4NywicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNjIyLTI3NGMyNzI1LTAwNDMtNGJlMS04Yzc3LWI5NWE1MTMwZWZlNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjU0NDdaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iYjZlNzE5ZTY4ZjFkNDQxY2NjNTVjYjVjZTUwMWY4ZDE1MjkyNGU2M2E4NDJmMjUxNmJkMzEwYTc3MzM4MzllJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.q9nZcFBkAGb4m3g2twHgguTNtDRNQXLLEy3fTEvhwto)

 5. Profit Margin

        % Margin = [Total Profit]/[Total Sales]

 ![Snap_5](https://private-user-images.githubusercontent.com/219225965/462771660-613f56c1-22d6-488b-8042-69616eb3df2f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjA0MjQsIm5iZiI6MTc1MTcyMDEyNCwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNjYwLTYxM2Y1NmMxLTIyZDYtNDg4Yi04MDQyLTY5NjE2ZWIzZGYyZi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjU1MjRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01OGNmMWVhZTJlZDRlYjRhZTRhYWJkMzBkN2M5ZjNmMDViYzg4NTcxOTRkMTVmYTlmYTFlNzNiY2Y0OWQyNDk3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.t7GfsHlFvbCzc85DpR6B8J7EIg1vMnYsuTYTKRHwjRA)
 
 # Report Snapshot (Power BI DESKTOP) (Overall View)

 
![Dashboard_upload](https://private-user-images.githubusercontent.com/219225965/462771753-0f7a8949-88d4-4faa-b4c9-28713b48a0c3.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjA1MDYsIm5iZiI6MTc1MTcyMDIwNiwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNzUzLTBmN2E4OTQ5LTg4ZDQtNGZhYS1iNGM5LTI4NzEzYjQ4YTBjMy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjU2NDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01YWRhNDlmNjIxNjE4YWE1MWM2NTBkYzkzZTcyYjU0NjczNWM3NThhOTFkZDgwZDM0ZTVmMzFkYTcxYjIyOThlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.wnbOWFmDxtKMOLovxJ4kG4SHtP8TZukQ8btcMJ9G5Uc)


 # RFM Analysis

 ![RFM_Analysis](https://private-user-images.githubusercontent.com/219225965/462771795-5eec1dc1-394f-4601-992b-57f50b03a931.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE3MjA1NDIsIm5iZiI6MTc1MTcyMDI0MiwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNzcxNzk1LTVlZWMxZGMxLTM5NGYtNDYwMS05OTJiLTU3ZjUwYjAzYTkzMS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNVQxMjU3MjJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04OTJjMWQzMDRjNGU0ZTRiM2ZiODA4MDQyNzQ1NzRhODI1ZTgyODRjMWQ3OTM5YjMzMTFhODI1N2QxMGFiZjk1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.u600n9wIvytGKi5LxEgM7bBJFmr0lJHiiOzC79R_k2s)


# Insights

A eight page report was created to understand better insights of the store.

Following inferences can be drawn from the dashboard;

### [1] Overall View

   Total Revenue: $2.12 M       
   Total Profit:  $286.4 K       
   Quantity:   $38 K         
   Monthly Orders:  462        
   Monthly Revenue: $96.67 K     


           
### [2] RFM Analysis

        Average Recency: 1.43 K
        Average Frequency: 12.6
        Average Monetory: $2.90 K
  
   

  ### [3] Profit Analysis
  
      % Margin: 12.5 %
      Total Profit: $286.4 K

  ### [4] New Customers and Top Salespersons

      Total Sales(New Customers): $ 7.51 K
      Total Quantity(New Customers): 148
      Total Discount(New Customers): $ 5.00

      

 
